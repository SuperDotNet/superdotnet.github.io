---
title: The Ubiquitous Bridge
author: Mike-EEE
type: post
date: 2015-10-01T20:29:41+00:00
excerpt: 'The Bridge to .NET Ubiquity: The Ubiquitous Bridge. In this article, we examine the current value proposition from Microsoft and explore a possible solution for a ubiquitous .NET client application development model offering.'
url: /2015/10/the-ubiquitous-bridge/
featured_image: /wp-content/uploads/2015/09/Transpile.png
mythemes-thumbnail-height:
  - 45
dsq_thread_id:
  - 4165084346
categories:
  - Developers-Win
  - General
series:
  - The Bridge to .NET Ubiquity

---
<div class="seriesmeta">
  This entry is part 6 of 6 in the series <a href="/series/bridge-to-dotnet-ubiquity/" class="series-6" title="The Bridge to .NET Ubiquity">The Bridge to .NET Ubiquity</a>
</div>

### TL;DR: VOTE!

This series exists to build support around the idea of a ubiquitous .NET client application development model. This is not intended to be a final solution, but a starting point for discussion, awareness, and a sign of demand. Show your support by voting for this idea here:

<div class="push-button-container"><div class="push-button">
</div><a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10027638-create-a-ubiquitous-net-client-application-develo" target="_blank"><div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;"></div><img class="push-button-vote-text" src="http://uploads.webflow.com/55e079ccd960e71226582014/55d09ab72123fb7e3e46b1cd_Vote%20Now!%20Text.svg" /></a></div>

### The Final Chapter

<a href="/2015/10/the-backwards-bridge/" target="_blank">So far in this series</a>, we have spent a considerable amount of time discussing the problems and challenges currently facing .NET client application developers.  In this article, we move to provide one possible solution towards addressing these problems while also providing a revenue driver for Microsoft.  This solution is not intended to be a final directive or instruction, but meant to promote discussion and dialogue around this very important and significant problem.

To date, we have seen how Microsoft is providing both broken guidance along with backward technologies for its developers.  So, what is the solution to these problems?  If the current strategy is backwards, then what is forwards?  If the current bridge to ubiquity is broken, then how do we fix it?  How is it possible to bring seemingly incompatible models together while still providing revenues for Microsoft&#8217;s bottom line?  How can Microsoft please both .NET and web developers, in addition to their shareholders?  Fortunately, the solution is much easier to describe than the problem itself.

### The Key Power of Transpilation

The answer here starts with how projects are compiled in .NET solutions.  Microsoft can solve all of these problems by adjusting how .NET projects are compiled and deployed.  This is done through a process known as transpilation and the use of a [JavaScript transpiler][1].

In this world, .NET developers continue to use their .NET solutions, and define their components and shared code in ways that are familiar to them.  When it is time to deploy their project, they transpile their results into web-friendly and HTML5 standard-compliant artifacts, the results of which can then further be deployed to a website or cloud provider.

This might sound like fairy tale or wishful thinking, but this idea is closer to reality than you might realize.  We invite you to [check out JSIL.org][2].  You can see there that this has been possible for some time now.  Indeed, it seems some whiz-kid out in California has been doing the work of what should be an entire Microsoft division since 2011 and enabling exactly this scenario.

Furthermore, projects such as [CSHTML5][3] (a product based on JSIL) and [Duoco.de][4] are also enabling and building towards this type of development paradigm.

But, they are not Microsoft, and they do not have Microsoft’s resources – or better, Microsoft’s authority.  What we are endorsing here is a fundamental cultural shift within Microsoft to take advantage of and promote this powerful strategy and resulting paradigm.  Microsoft should either acquire and/or partner with the companies and efforts above to make this happen.

**_By embracing a .NET-to-JavaScript transpilation strategy and supplementing its compiled cross-platform strategy, Microsoft can successfully enable a ubiquitous .NET client application model._**

This means compiling and transpiling Universal Windows Platform (and even WPF and WinForms too, if we get ambitious) applications so that they can be deployed, hosted, and rendered in the following platforms and environments:

  * iOS and Macintosh (native)
  * Droid and *nix (native)
  * HTML5/JS (web)

### The Current Value Proposition

<a href="https://dev.windows.com/en-us/Registration/AccountInfo" target="_blank">Part of the reason why Microsoft can get away with charging developers $19 and companies $99</a> is loosely based on the promise to reach 1 billion installs of Windows 10 by 2018.  And they should.  Windows 10 is a great product.  The value proposition is “give us $19, and we will give you access to a marketplace of 1 billion users.”

One billion users might seem a lot – and it is – but it is not the entire device market.  In fact, according to [Xamarin’s keynote from a year ago][5] (featured 06:17 in), there are approximately 1.6 billion non-Microsoft devices (tablets and phones) circulating in the marketplace as of 2014.  By 2018, this number should jump even more, but for the sake of our discussion here we will round it out to a conservative 1.5 billion.  This is still more than what Microsoft claims it will reach in a best case scenario for Windows 10 installations by 2018, by 150%.  That means that even if Windows 10 reaches 1 billion installs, there will still be approximately 1.5 billion devices out there that Windows developers cannot reach with their application.  To see what this looks like, please see the chart below based off data provided by the above keynote and pairing it with data provided by <a href="http://www.netmarketshare.com/" target="_blank">Net Market Share</a> from <a href="http://www.netmarketshare.com/report.aspx?qprid=8&qptimeframe=M&qpsp=187&qpch=350&qpmr=100&qpdt=1&qpct=3&qpcustomd=1&qpcid=fw17131&qpf=1" target="_blank">August 2014</a> to <a href="http://www.netmarketshare.com/report.aspx?qprid=8&qptimeframe=M&qpsp=199&qpch=350&qpmr=100&qpdt=1&qpct=3&qpcustomd=1&qpcid=fw17131&qpf=1" target="_blank">August 2015</a>, and projecting it to 2018, when Microsoft expects to reach 1 billion installs of Windows 10:

<a name="MarketReach"></a>

<div id="attachment_275" style="width: 1034px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2015/09/20150923021143.png"><img class="wp-image-275 size-large" src="/wp-content/uploads/2015/09/20150923021143-1024x753.png" alt="Chart demonstrating marketplace accessibility for various platforms." width="1024" height="753" srcset="/wp-content/uploads/2015/09/20150923021143-1024x753.png 1024w, /wp-content/uploads/2015/09/20150923021143-300x221.png 300w, /wp-content/uploads/2015/09/20150923021143-768x565.png 768w, /wp-content/uploads/2015/09/20150923021143.png 1095w" sizes="(max-width: 1024px) 100vw, 1024px" /></a>
  
  <p class="wp-caption-text">
    Estimated technology platform reach up to 2018.  Behold, HTML5&#8217;s Wall of Ubiquity.
  </p>
</div>

Any projections into the future comes with its own set of risks and inaccuracies.  What we are attempting to do here is to not only show the fragmented market that exists (and will exist), but also just how much reach Microsoft can ultimately hope to attain when compared with outstanding platforms and technologies.  The other very obvious observation here is the &#8220;Wall of Ubiquity&#8221; that we see represented by HTML5.  While client application models might work for a particular platform, a HTML5-compliant client application model will work on _any device in the market place_, assuming that device is equipped with an HTML5 browser (and we are assuming most if not all are).

By looking at the chart above, which area would you expect to pay $19 (or more) for access?  <a href="http://www.techrepublic.com/blog/software-engineer/app-store-fees-percentages-and-payouts-what-developers-need-to-know/" target="_blank">Or $25</a>?  <a href="http://www.techrepublic.com/blog/software-engineer/app-store-fees-percentages-and-payouts-what-developers-need-to-know/" target="_blank">Or even $99 <em>annually</em></a>?  By all accounts, the HTML5 would seem to be the market that would require such fees, but it alone is the only freely accessible market in our chart.  As developers, we must collectively at some point ask ourselves if this makes logical and business sense, and why we are paying for an exclusive market when a free, ubiquitous market exists that dwarfs any comparable market out there.

### The Aligned Value Proposition

To this point, we have seen how Microsoft charges $19 for access to their exclusive and hypothetical market of 1 billion devices.  To us, this doesn&#8217;t make very much sense as we can develop an HTML5 application for free that will reach a much bigger, ubiquitous market.  It doesn&#8217;t make sense to pay $19 for access to a limited, exclusive market.  However, what does make sense is to provide the capability to take an exclusive-market application and enable it for other markets &#8212; exclusive, ubiquitous, or both.

In the case of an individual developer, imagine a world where Microsoft not only charges developers $19 to access a marketplace of 1 billion Windows 10 installs with their Universal Windows Platform applications, but additionally provides those developers with the ability to reach the 1.5 billion non-Microsoft market (via cross-platform compilation) with the exact same application for an additional $19*2 (for Droid and iOS), and an additional $19 for transpiling their UWP application into HTML5/JS artifacts to host on the web ubiquitously.

In this world, Microsoft could be pulling in up to (at least) $76 per developer or $396 per company – per registration, or more if they make this an annual fee (and their stockholders would probably agree they should).

Here, the value is clear.  Developers and organizations that want a ubiquitous, cross-platform .NET client application will be _more than willing_ to pay for these registrations, as they now get to leverage all of their existing code, training, and investments while building in a familiar client application model that makes the most sense to them, all the while leveraging the ubiquity that comes with cross-platform and global accessibility.

What’s more, Microsoft shareholders (or potential investors) see another viable (and potentially significant) revenue stream to pad their earnings.

Microsoft .NET client developers win, Microsoft shareholders win, Microsoft Wins.

<div id="attachment_328" style="width: 641px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2015/09/Vision.png"><img class="size-full wp-image-328" src="/wp-content/uploads/2015/09/Vision.png" alt="The Vision of a Ubiquitous .NET Client Application Development Model" width="631" height="434" srcset="/wp-content/uploads/2015/09/Vision.png 631w, /wp-content/uploads/2015/09/Vision-300x206.png 300w" sizes="(max-width: 631px) 100vw, 631px" /></a>
  
  <p class="wp-caption-text">
    The Vision of a Ubiquitous .NET Client Application Development Model
  </p>
</div>

### Hey, This Sounds Familiar…

For those reading this and think this sounds like it is pulling a page right out of [Xamarin’s][6] playbook, that is because it is.  This is indeed a successful model currently being employed by Xamarin.  Xamarin does offer amazing cross-platform support in the way of middleware.  However, as we have already visited,  Xamarin offers _an adaptive client application model_ that differs from UWP, WPF, and WinForms.  In an adaptive client application model, the applications that get built _adapt_ to the target platform and render as that platform’s built-in user interface and controls, and its subsequent user experience.

Conversely, the vision here is to have a full-fidelity, exact port of of a .NET client application model that is like (or is) Universal Windows Platform (or WPF / Window Forms) to other target platforms, leading to a consistent look and feel for applications of these models, no matter where they are run.  This satisfies our consistent user interface requirement and aligns itself with the nature of the web, where a web page (which is ultimately a view within a hosted application) views and operates the same no matter what device or platform used to view it.

That does not necessarily mean that this strategy is at odds with Xamarin.  On the contrary, Microsoft should leverage its partnership with Xamarin to assist with the tooling and support required to build for the different supported platforms.  Profit sharing from registrations due to this could and should most undoubtedly occur.

### Take Action

Our ideas above are merely that, ideas.  We possess but one suggestion to enable a ubiquitous .NET application model, and it comes from a perspective that is the result of being immersed in .NET development for over 15 years.  There may be other market forces or considerations at play here that we have not considered, and we are open to feedback, discussion, and dialogue around our proposal.

At the end of the day, the purpose of this series is to build awareness around and direction towards a ubiquitous .NET client application model.  <a href="http://dotnetfuture.wufoo.com/forms/m1azjhyi1ozawho/" target="_blank">We have had these ideas for a while in one form or another now</a>, since the death of Silverlight in 2011.  This article is also the result of many postings and conversations held and read on Twitter, .NETFoundation, GitHub, and yes especially UserVoice.

Developers Win! is all about garnering support around important issues, and around this issue in particular.  It is primarily why we started this site and why we exist.  We have created a vote around this issue and you can vote for it by clicking on our awesome vote button here:

We also encourage you to provide your input in the comments below.  Thank you for your consideration and support in advancing a future where Developers Win!

<div class="push-button-container"><div class="push-button">
</div><a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10027638-create-a-ubiquitous-net-client-application-develo" target="_blank"><div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;"></div><img class="push-button-vote-text" src="http://uploads.webflow.com/55e079ccd960e71226582014/55d09ab72123fb7e3e46b1cd_Vote%20Now!%20Text.svg" /></a></div>

 [1]: https://en.wikipedia.org/wiki/Source-to-source_compiler
 [2]: http://jsil.org
 [3]: http://cshtml5.com
 [4]: http://duoco.de
 [5]: https://evolve.xamarin.com/
 [6]: http://xamarin.com