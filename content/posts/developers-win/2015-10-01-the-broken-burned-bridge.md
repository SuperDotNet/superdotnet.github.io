---
title: The Broken, Burned Bridge
author: Mike-EEE
type: post
date: 2015-10-01T20:23:08+00:00
excerpt: 'The Bridge to .NET Ubiquity: The Broken, Burned Bridge. In this article we explore the broken bridge (via guidance) that Microsoft has given in response to 16,000 votes for Silverlight 6.'
url: /2015/10/the-broken-burned-bridge/
featured_image: /wp-content/uploads/2015/09/Transpile.png
mythemes-thumbnail-height:
  - 45
dsq_thread_id:
  - 4165083650
categories:
  - Developers-Win
  - General
series:
  - The Bridge to .NET Ubiquity

---
<div class="seriesmeta">
  This entry is part 4 of 6 in the series <a href="/series/bridge-to-dotnet-ubiquity/" class="series-6" title="The Bridge to .NET Ubiquity">The Bridge to .NET Ubiquity</a>
</div>

### TL;DR: VOTE!

This post exists to build consensus in the Microsoft developer community around the idea of a ubiquitous .NET client application development model.  Show your support by voting for this idea here:

<div class="push-button-container"><div class="push-button">
</div><a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10027638-create-a-ubiquitous-net-client-application-develo" target="_blank"><div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;"></div><img class="push-button-vote-text" src="http://uploads.webflow.com/55e079ccd960e71226582014/55d09ab72123fb7e3e46b1cd_Vote%20Now!%20Text.svg" /></a></div>

### The Burned Bridge

In July 2015, Microsoft closed and responded to a vote for [Silverlight 6 that amassed an impressively astounding 16,000 votes][1] (note that the current value is due to votes being returned to users).  Their answer: just use HTML5 instead.  To say that this is a shocking directive is an understatement.  [As we have (hopefully) demonstrated so far][2], HTML5 (or web client development) offers a completely different client application model than a .NET client application model.  What’s more, HTML5 is not a Microsoft property.  So, why is Microsoft directing its own developers to use technologies that are outside of its intellectual property portfolio (keep in mind that Microsoft does not offer its own client-hosted client application model solution)?  This answer – which we call “The Broken Bridge” – is just as confusing as it is expensive, and in this article we aim to illustrate how it is exactly both.

### Conceptual and Architectural Problem

First, let’s start with the fundamentals by way of a simple example with a typical .NET solution.  In this .NET solution, you will find projects organized by server, client, and finally shared code between the two.  In shared code projects, you will usually find components that can be used in both application boundaries.  A good example of a shared component is an `ExceptionFormatter`, which can be used to format an exception that occurs within an application into a desired format that can then further be sent to a logging provider (which in turn could also be another shared component) for instrumentation or logging purposes.

<div id="attachment_271" style="width: 222px" class="wp-caption alignleft">
  <a href="/wp-content/uploads/2015/09/dotNet.png"><img class="wp-image-271 size-medium" src="/wp-content/uploads/2015/09/dotNet-212x300.png" alt="ExceptionFormatter in a typical .NET solution." width="212" height="300" srcset="/wp-content/uploads/2015/09/dotNet-212x300.png 212w, /wp-content/uploads/2015/09/dotNet.png 242w" sizes="(max-width: 212px) 100vw, 212px" /></a>
  
  <p class="wp-caption-text">
    Our ExceptionFormatter in a typical .NET solution.
  </p>
</div>

In the world of .NET application development, `ExceptionFormatter` happily lives on both server and client applications, and each application boundary will have the same compiled version upon deployment.  The component has its own set of unit tests assigned to it and whenever something unexpected occurs in its behavior in (either on the server-side or the client), the unit tests are adjusted accordingly and the component _benefits and improves from usage in both application boundaries_.

Now, let’s say we follow the directive provided by Microsoft in the closed Silverlight 6 vote above and move our client application from a .NET client application into a new HTML5 web client application so that it can take advantage of the web’s ubiquity.  Keep in mind that Microsoft is not offering a solution here, but instead instructing developers to simply “use HTML5 instead.”

<div id="attachment_272" style="width: 310px" class="wp-caption alignright">
  <a href="/wp-content/uploads/2015/09/Html5ExceptionFormatter.png"><img class="size-medium wp-image-272" src="/wp-content/uploads/2015/09/Html5ExceptionFormatter-300x252.png" alt="ExceptionFormatter in an HTML5 Client Application and .NET Server" width="300" height="252" srcset="/wp-content/uploads/2015/09/Html5ExceptionFormatter-300x252.png 300w, /wp-content/uploads/2015/09/Html5ExceptionFormatter.png 371w" sizes="(max-width: 300px) 100vw, 300px" /></a>
  
  <p class="wp-caption-text">
    ExceptionFormatter in an HTML5 Client Application and .NET Server
  </p>
</div>

In doing so, we can no longer use our .NET shared code assembly, _as our compiled .NET assembly cannot be used in a HTML5 application in any way_.  In the case of our `ExceptionFormatter`, we have to write it again in either JavaScript or (&#8220;better yet&#8221;) <a href="http://www.typescriptlang.org/" target="_blank">TypeScript</a>.  But now, we have **two** `ExceptionFormatters` in our solution: one in our .NET server application boundary and one in our HTML5 client application boundary.  _Now, each version must have its own set of code and testing built around it_.  If an inerrant behavior is now caught in one application boundary, it must be accounted for (if applicable) in the other, and vice versa.

If this sounds to you like it is violating a design principle of some sort, then pat yourself on the back, dear developer.  It is known as [Don’t Repeat Yourself (DRY)][3] and it is a principle that is used throughout tried-and-true quality software development.  It is more appropriately and technically known as [encapsulation][4], and when used properly, it yields one of the highest forms of quality found in any software solution deployed today.

By providing two versions of the same conceptual object (one in the server written in .NET, and one in the client written in JavaScript), application developers are now violating DRY and having to double their efforts in development, maintenance, and quality assurance.  Not to mention, the organizations who employ them are having to pay for this training and management as well.

### Organizational and Resource Problem

That leads to another big problem due to the existence of this broken bridge.  Organizations now have to make difficult decisions for the type of technology to use for their client applications, and every single one of them are having to face this expensive decision as outlined above.  As a result, solutions that had a unified codebase in .NET are now having to be bifurcated between .NET in the server boundary, and HTML5/JavaScript in the client boundary.  Additionally, organizations must now either train and/or hire resources that can develop these client web applications.  This now means that organizations that were once experts in one technology are now becoming generalists in two.  Because of this, they are having to pay the difference between the quality of code written by experts (higher-quality) and generalists (lower-quality).

Add the cost of maintaining two codebases that violate DRY (along with its redundant, overlapping concerns) with the cost of reducing expert organizational resources to generalists, and it is fair to say that organizations now face an expensive problem.  By following Microsoft’s guidance above and putting their feet into both worlds, organizations now incur an expensive cost in overhead and architecture that simply does not exist in solutions where the client application model is compatible and unified with the server application model.

### Dangerous Directive

By directing developers and organizations to “just use HTML5,” Microsoft is leading them both down an expensive and dangerous path.  This neither makes business sense, nor does it benefit Microsoft or the developers its supposed to serve.  In fact, it may force savvy technology firms to abandon Microsoft technologies altogether and become exclusively based in JavaScript-based solutions.  Unfortunately, you might have already seen chatter online where this <a href="http://forums.dotnetfoundation.org/t/cross-platform-wpf/421/71" target="_blank">already become an actualized reality with some developers</a>.  If left unanswered, it is only a matter of time before entire organizations follow their lead.

### Show Your Support

If you like the idea of a ubiquitous .NET client application development model, please take the time and let Microsoft know by voting for this idea on UserVoice now:

<div class="push-button-container"><div class="push-button">
</div><a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10027638-create-a-ubiquitous-net-client-application-develo" target="_blank"><div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;"></div><img class="push-button-vote-text" src="http://uploads.webflow.com/55e079ccd960e71226582014/55d09ab72123fb7e3e46b1cd_Vote%20Now!%20Text.svg" /></a></div>

 [1]: visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/3556619-silverlight-6
 [2]: /2015/10/existing-net-client-application-models/#html5
 [3]: http://c2.com/cgi/wiki?DontRepeatYourself
 [4]: https://en.wikipedia.org/wiki/Encapsulation_(computer_programming)