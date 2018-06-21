---
title: Investigating Weird Result Times in Benchmark.NET
author: Mike-EEE
type: post
date: 2018-05-25T13:07:40+00:00
url: /2018/05/investigating-weird-result-times-in-benchmark-net/
mythemes-thumbnail-height:
  - 45
categories:
  - Developers-Win
  - General

---
### TL;DR

I&#8217;ve spent the past year or so by way of 100 collective hours wrestling with a JIT-related code alignment issue which is now being tracked on both the <a href="https://github.com/dotnet/BenchmarkDotNet/issues/756" target="_blank" rel="noopener">Benchmark.NET</a> and <a href="https://github.com/dotnet/coreclr/issues/17932" target="_blank" rel="noopener">.NET Core</a> repositories.

### Why Are You Out of Your Foxhole?!

As you may or may not know, I am not a big fan of blogging.  Well, not personally, at least.  It takes a lot of energy and I would rather put that energy into coding &#8212; where it belongs!  So, why am I taking time to do something mundane as share [my thoughts around //build 2018][1] and write _even more things I might immediately regret_ to produce yet another article here for you?

<div style="width: 410px" class="wp-caption aligncenter">
  <img class="size-large" src="https://i.imgur.com/Q81RPrp.gif" alt="Me seen here after posting a blog post." width="400" height="225" />
  
  <p class="wp-caption-text">
    TFW you post a blog instead of sticking to the codez.
  </p>
</div>

Did I have a change of heart?  Not really, but, in short, I will say that I have been _completely_ derailed on an issue that has taken a good amount of time to diagnose (having three different forms when combined over the course of the past year) and I thought I would do a bit of a retrospective here to bring closure to this most difficult time. 😂

### SO GET TO IT, MAN!

Alright, it&#8217;s actually very difficult to articulate, but the short of it is that when running <a href="https://github.com/dotnet/BenchmarkDotNet" target="_blank" rel="noopener">Benchmark.NET</a> benchmarks, results will vary by 10-15% with the smallest of changes in code.  Additionally, if one was not paying close attention (i.e. overly obsessive and quite possibly a tad OCD 🤔) then it was very easy to over look this very strange phenomena as the times are off by a slim margin and difficult to perceive unless you are really locked into spotting it.

For me, this all began a little over a year ago, when I started to experience some very peculiar (and very subtle) anomalies while running some Benchmark.NET performance testing for my contributions to <a href="https://extendedxmlserializer.github.io/" target="_blank" rel="noopener">ExtendedXmlSerializer v2</a>.  These anomalies would seem to be fixed, _only to return after I ended up writing more code_ and _writing more code that had nothing to do with the code being benchmarked_.  We are talking Grade A Insanity Fodder here.

The pattern ran as such:

  1. Identify poor performance.
  2. Change some code.
  3. Notice better performance.
  4. Change/add/remove some code _that had nothing to do with the code being benchmarked_ (e.g. comment out a class altogether)_._
  5. Notice different result times (could be better, could be worse).

I thought for sure there was something wrong with my machine &#8212; it was overclocked, and it was running Windows Server, with the images from several upgrades images from Windows 8.0.  I was also running tests within a Virtual Machine and this is also known to impact results (although this was a different issue altogether).

So I formatted my server and reinstalled everything from scratch.  In the end, I ended up being very uncharacteristic of myself and _abandoning the whole performance story all together_ because it was simply taking up too much time to diagnose.  Part of the problem was that I was using .NET Core 1.1 tooling and I thought for sure there might be a latent bug lurking somewhere in there.  However, thinking it was mostly a Benchmark.NET issue, I managed to make a mess of their repository in my pursuit by setting up issues <a href="https://github.com/dotnet/BenchmarkDotNet/issues/330" target="_blank" rel="noopener">here</a>, <a href="https://github.com/dotnet/BenchmarkDotNet/issues/353" target="_blank" rel="noopener">here</a>, <a href="https://github.com/dotnet/BenchmarkDotNet/issues/433" target="_blank" rel="noopener">here</a>, and <a href="https://github.com/dotnet/BenchmarkDotNet/issues/739" target="_blank" rel="noopener">here</a>.

Fast forward a year later, and you find me trying out the latest .NET Core 2.0 magic (which is really quite incredible, btw! more below).  This involved getting all the latest versions of everything with up-to-date Windows OS software, the whole ordeal.  Despite all of this, guess what I manage to discover is still easily readily visible and lurking within Benchmark.NET?  That&#8217;s right, the very gremlin that is the subject of this entire ordeal.

This time, however, I was able to capture it with a simple LINQ `ToArray` call, and produce different variations of results from _the exact same code being benchmarked_.  While the actual benchmark code did not change, the results _differed_ if I added new attributes, or a different component such as the <a href="http://adamsitnik.com/the-new-Memory-Diagnoser/" target="_blank" rel="noopener"><code>MemoryDiagnoser</code>.</a>

If you are interested in seeing these different variations, <a href="https://github.com/Mike-EEE/BenchmarkDotNet.InProcess" target="_blank" rel="noopener">you can start here</a>.  Note <a href="https://github.com/Mike-EEE/BenchmarkDotNet.InProcess/tree/TheWeird_05" target="_blank" rel="noopener">this branch</a> especially which demonstrates this issue simply by adding a `System.ComponentModel.DescriptionAttribute` (!) to <a href="https://github.com/Mike-EEE/BenchmarkDotNet.InProcess/tree/TheWeird_04" target="_blank" rel="noopener">this branch</a> (you can see the result times from their respective READMEs).  Additionally, note that this issue occurs when you keep the `BenchmarkDotNet.Artifacts` folder on the local system disk versus deleting it.

Additionally, for a _much simpler_ reproduction of this issue, you can <a href="https://github.com/Mike-EEE/DotNetCore.CodeAlignment" target="_blank" rel="noopener">see my simple reproduction application here</a> along with <a href="https://github.com/Mike-EEE/DotNetCore.CodeAlignment.Alternate" target="_blank" rel="noopener">an alternate version here</a>.  These make use of the `BenchmarkSwitcher` to easily go through different cases and demonstrate the different times.

### What On Earth is Going on Here?

In the spirit of trying to keep the amount of time I have invested into this to under 110 hours 😉, I was fortunate to discover that upgrading between .NET Core 2.0 and .NET 2.1 produced this error _without any additional code changes_.  Aha!  At this point, I knew for certain that I was no longer dealing with a Benchmark.NET-specific issue, but rather, some odd behavior in the .NET Core CLR/SDK/Tooling.  So, I set up the Bat Signal on their repository to see what the deal was.  You can <a href="https://github.com/dotnet/coreclr/issues/17932" target="_blank" rel="noopener">follow along here</a>.  A big shout out to <a href="https://github.com/mikedn" target="_blank" rel="noopener">@mikedn</a> for taking the time and having the patience to walk through this with me.  I thought for sure I was crazy, but it turns out that I am not &#8230; well, as far as this particular issue is concerned, that is. 🎉

When the dust settled, it appears that we are looking at a JIT-related code alignment issue, and <a href="https://github.com/dotnet/BenchmarkDotNet/issues/756" target="_blank" rel="noopener">one that is now being tackled by the Benchmark.NET team</a>.  Additionally, I was able to find a workaround for the interim to get me unblocked.  So I am finally free to code again.  WHEW! 😌😂

### The Awesome State of the Current .NET Ecosystem

With all of that out of the way, I did want to take a second to send a shout out to the current state of the .NET ecosystem.  Just how awesome is it right now?!  You know, it used to be that you would go on Connect, wait a full day for the page to load (or whatever was/is going on there), then wait a full month for their team to figure out a reason _not_ to fix your issue, and then have them return with the lame excuse to relay to all the people who have voted to have that issue fixed.  (<a href="https://docs.microsoft.com/en-us/collaborate/connect-redirect" target="_blank" rel="noopener">Turns out that Connect has been sunsetted</a>, as it should be &#8212; it&#8217;s too bad as I had some great examples of closing issues without a whole lot of merit.)

These days, you have full _collaborative_ exposure to the _entire team_ that is building the product in which you are having a problem and really have some awesome conversations and insight into the entire process!  It&#8217;s really amazing.  AND if you feel so daring you can actually contribute with your own pull requests and _actually make a difference_.

Now THAT is <a href="https://vimeo.com/98720197" target="_blank" rel="noopener">making the world a better place</a>. 😉

And, I am not sure if you frequent blog posts, but the .NET team also does a terrifically amazing job of being very engaging and interactive with their developers and customers.  Maybe it&#8217;s been like this for years and I haven&#8217;t noticed?  There&#8217;s also Twitter, as well.  But, I find Twitter to be cumbersome and awkward &#8212; not to mention, EVIL! 🤣  Sorry, but I cannot be constrained by x-characters and require freedom to expression!  But, regardless of your medium, it&#8217;s fantastic to see such a transparent, open, and engaging community and process these days.  Let&#8217;s hope it only gets better from here (although I am not sure how it can!).

Some notable performance/.NET shout outs (in order that they arise to me, don&#8217;t hold it against me!):

  * <a href="https://github.com/wojtpl2" target="_blank" rel="noopener">Wojciech Nagórski</a>: For putting together <a href="https://extendedxmlserializer.github.io/" target="_blank" rel="noopener">ExtendedXmlSerializer</a> to make this whole adventure possible.
  * <a href="https://twitter.com/andrey_akinshin" target="_blank" rel="noopener">Andrey Akinshin</a>, <a href="https://twitter.com/SitnikAdam" target="_blank" rel="noopener">Adam Sitnik</a>, and <a href="https://twitter.com/matthewwarren" target="_blank" rel="noopener">Matt Warren</a>: For your efforts towards Benchmark.NET, truly a transformative application and asset for our community.
  * <a href="https://github.com/mikedn" target="_blank" rel="noopener">mikedn</a>: I appreciate your help so much you get two mentions. 😁
  * <a href="https://github.com/stephentoub" target="_blank" rel="noopener">Stephen Toub</a>: For being as attentive to feedback as you are <a href="https://blogs.msdn.microsoft.com/dotnet/2018/04/18/performance-improvements-in-net-core-2-1/" target="_blank" rel="noopener">meticulous in your writings</a>!
  * <a href="https://github.com/AndyAyersMS" target="_blank" rel="noopener">Andy Ayers</a>: For your insight, assistance, and engagement with the community.
  * <a href="https://stackoverflow.com/users/175070/mike-strobel" target="_blank" rel="noopener">Mike Strobel</a>: While I have the horn out, a massive shout out to all your research on <a href="https://stackoverflow.com/a/50261522/3602057" target="_blank" rel="noopener">my performance question on StackOverflow</a>!
  * <a href="https://twitter.com/terrajobst" target="_blank" rel="noopener">Immo Landwerth</a>: Not really related to this issue, but wanted to send a quick shout out to thank you for managing .NET the way it _should_ be. 😊

### FIN

OK&#8230; enough of this writing business.  Now, where was that foxhole of mine&#8230; 🦊  IT&#8217;S TIME TO CODE AGAIN Y&#8217;ALL!!!

 [1]: /2018/05/thoughts-on-build-2018-and-why-scottgu-should-be-msft-ceo/