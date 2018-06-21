---
title: 'The Great .NET Client Divide: A Simple Example (Hopefully)'
author: Mike-EEE
type: post
date: 2016-02-08T12:31:51+00:00
excerpt: In this article, we explore the problem facing .NET developers who wish to host their applications in the web.
url: /2016/02/the-great-net-client-divide-a-simple-example-hopefully/
mythemes-thumbnail-height:
  - 45
dsq_thread_id:
  - 4561618700
categories:
  - Developers-Win
  - General

---
### TL;DR: Vote!

I have been getting some good feedback on <a href="/series/bridge-to-dotnet-ubiquity/" target="_blank">writing lengthy blog articles</a>. Right right. I try to be aware and respectful of your time.  And mine, too. At the end of the day I am just some random developer that you don&#8217;t know who happens to put their thoughts on the web &#8212; and I try to keep that in mind.  Additionally, I simply _hate_ writing and _hate_ writing long articles even more, so your guess is as good as mine as to why I put myself (and you, the patient reader) through so much agony. With that said, let&#8217;s see if I can keep this short.  Please vote:

<div class="push-button-container"><div class="push-button">
</div><a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10027638-create-a-ubiquitous-net-client-application-develo" target="_blank"><div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;"></div><img class="push-button-vote-text" src="http://uploads.webflow.com/55e079ccd960e71226582014/55d09ab72123fb7e3e46b1cd_Vote%20Now!%20Text.svg" /></a></div>

### What Is It Now?

I have been checking out some awesome logging software lately, namely <a href="http://serilog.net/" target="_blank">Serilog</a> and a (just as awesome) complimentary logging presentation component, <a href="http://getseq.net/" target="_blank">Seq</a>. I have to say that Serilog is the real deal. Just look at all these sinks, <a href="https://github.com/serilog/serilog/wiki/Provided-Sinks" target="_blank">JUST YOU LOOK AT THEM!</a> That is some serious business. You can also use an <a href="https://github.com/serilog/serilog/wiki/Configuration-Basics" target="_blank">amazing configuration fluent API</a> which just might change the way I approach all my future solutions &#8212; I&#8217;ve seen fluent, but not like _this_.  <a href="https://www.youtube.com/watch?v=EnJk39QSujA" target="_blank">This means something, this is important</a>!

### So What Is the Problem?

Serilog is an awesome .NET logging solution.  It will work in a .NET application on the server (where you can also use in conjunction with Seq), and it will work in a [WPF application][1] or even [WinForms application][2] (again, with Seq).  It will work in a Console Application (with Seq), and there is <a href="http://nblumhardt.com/2016/02/serilog-2-0-progress-update/" target="_blank">even an effort to allow it to work in a .NET Core application</a> (Seq TBD).

### GET TO THE PROBLEM, DAMN YOU!!!

I as a .NET developer can use Serilog in all of the aforementioned application types, but [if I follow Microsoft Leadership&#8217;s guidance and use a NodeJS application on top of a .NET server application][3], I cannot use Serilog as <a href="https://github.com/serilog/serilog/issues/657" target="_blank">it does not have an official JavaScript port</a>.  I can use an [unsupported version][4] that is &#8220;like&#8221; it (and it doesn&#8217;t even feature the same name), but it is not following the same version (or capability) cadence &#8212; <a href="https://github.com/structured-log/structured-log/issues/1" target="_blank">and let&#8217;s not forget I want to preserve the Seq awesomeness</a>!

### <a href="https://youtu.be/GVHPEJoMGsY?t=20s" target="_blank">Ahhhhhhh</a>&#8230;  I get it.

Am I interviewing myself again?  I hate when that happens.  Anyways, to &#8220;fix&#8221; this problem, Serilog must either create a feature parity and version-synchronized JavaScript API (<a href="http://reactivex.io/" target="_blank">like a major product</a>), or I as a developer must look for another equivalent of Serilog in the JavaScript/NodeJS ecosystem &#8212; written by a completely different developer (or developers) with a different style and approach and having to context-switch between the two (JavaScript and .NET).  <span style="line-height: 1.5;">In either case, this is additional (read: <span style="text-decoration: underline;"><em><strong>A LOT OF</strong></em></span>) work and the resulting solution will end up having two &#8220;Serilogs&#8221; which </span><a style="line-height: 1.5;" href="/2015/10/the-broken-burned-bridge/">essentially breaks encapsulation and DRY</a><span style="line-height: 1.5;">.</span>

### Worse Yet

Even worse, I can [choose to ditch .NET altogether][5] and [simply use a NodeJS JavaScript solution for client and server applications][6] as this design features code reuse between the two tiers.

### <a href="http://www.nooooooooooooooo.com/" target="_blank">NOOOOOOOOOOOOOO!!!</a>

Exactly.

### WHEW!  Please Vote

I actually got this in at a little over 550 words.  Not bad.  If you would like to see a JavaScript version of Serilog (and _any_ .NET library, for that matter) seamlessly transpiled for _any_ .NET project at compile time as part of a ubiquitous .NET client application development model offering, please tell the Visual Studio team you would like to see this magic happen by voting for this issue right here:

<div class="push-button-container"><div class="push-button">
</div><a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10027638-create-a-ubiquitous-net-client-application-develo" target="_blank"><div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;"></div><img class="push-button-vote-text" src="http://uploads.webflow.com/55e079ccd960e71226582014/55d09ab72123fb7e3e46b1cd_Vote%20Now!%20Text.svg" /></a></div>

 [1]: /2015/10/existing-net-client-application-models/#windows-presentation-foundation
 [2]: /2015/10/existing-net-client-application-models/#windows-forms
 [3]: /2015/12/is-net-in-trouble-belated-thoughts-from-connect-2015/
 [4]: https://github.com/structured-log/structured-log
 [5]: /2015/10/the-broken-burned-bridge/#dangerous-directive
 [6]: /2015/12/is-net-in-trouble-belated-thoughts-from-connect-2015/#flocking-to-nodejs