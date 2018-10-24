---
title: The Backwards Bridge
author: Mike-EEE
type: post
date: 2015-10-01T20:27:57+00:00
excerpt: "The Bridge to .NET Ubiquity: The Backwards Bridge. In this article, we look into the backwards bridge of a failed strategy in Universal Windows Platforms's WinJS."
url: /2015/10/the-backwards-bridge/
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
  This entry is part 5 of 6 in the series <a href="/series/bridge-to-dotnet-ubiquity/" class="series-6" title="The Bridge to .NET Ubiquity">The Bridge to .NET Ubiquity</a>
</div>

### TL;DR: VOTE!

This series exists to build support around the idea of a ubiquitous .NET client application development model. This is not intended to be a final solution, but a starting point for discussion, awareness, and a sign of demand. Show your support by voting for this idea here:

<div class="push-button-container"><div class="push-button">
</div><a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10027638-create-a-ubiquitous-net-client-application-develo" target="_blank"><div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;"></div><img class="push-button-vote-text" src="/images/VoteNow.svg" /></a></div>

### Crossing Backwards

In [our last article][1], [we][2] looked at the current guidance that serves as Microsoft&#8217;s official answer to a ubiquitous web client application model, and have demonstrated how it is a failed a broken bridge to its destination.  In this article, we move on to another attempted bridge to web technologies, and hope to show it is as broken as it is backwards.  This is especially so when we consider its business model implications.

This bridge was built soon after Silverlight, when Microsoft introduced the “new” .NET that was created as a “complimentary replacement” (to use our own expression) to existing .NET and WPF applications.  Known as Windows Runtime (WinRT), this platform was the predecessor to UWP and introduced support for JavaScript under the [API name of WinJS][3].

One might look at that decision and admire the impressive feat of engineering that enabled a language like JavaScript into the .NET ecosystem.  And, they would be correct in this regard.  Another perspective might ask: _why?  Why even do this in the first place?_  If a developer has an HTML5 and JavaScript skillset that caters to a ubiquitous audience, what incentive do they have to build an application to host within the non-ubiquitous Windows Store when they can use that same skillset to build a ubiquitously-available web-hosted application?

To be sure: as of July 2015, Windows Store-compatible desktop and devices accounted for [_only 16% of the desktop market_][4]_._  So, what incentive does a web developer have to spend even one second towards building a solution that only reaches 16% of the desktop market when that same one second could be better used towards building a ubiquitously available application (which, incidentally, completely dwarfs the WinRT desktop market)?

Thankfully, in this case, logic seems to have won the day, as it seems a lot of web developers have asked this very question.  As a result, WinJS has failed to gain significant adoption.

### Backwards Thinking

But, this is not the end of it.  We continue to see this backwards-thinking strategy being employed by Microsoft to cater to Universal Windows Platform and to bring web development resources into .NET client development, _rather than the other way around_.  The latest attempt being [a JavaScript browser that runs as a Universal Windows Platform application][5].  Here again, we see the same theme.  Yes, it is neat to see such a combination and use of technologies, but the business challenge is the same: the opportunity cost in applying a HTML5/JS skillset towards making a WinJS application is significantly greater – _by factors_ – than applying that same skillset to making a ubiquitously-available web-hosted application.

Or again, asked as a question: why would a developer who can already reach ubiquity with their HTML5/JavaScript skillset risk the opportunity cost to regress and cater to a market that reaches a fraction of the ubiquity that they already enjoy?  _It simply does not make any business sense._

### Backwards Business Strategy

When viewed by the perspective of the typical web developer, the above value proposition is a headscratcher.  But when viewed through the lens of Microsoft’s current business model, it makes perfect sense.  Here’s why: in addition to claiming adoption for WinJS, Microsoft can also claim revenues from not only the developer, but also in the application that they create to host in the Windows Store.  In fact, in order to even register into the store, [an individual developer must pay $19.00 while a company must pay $99.00][6].  Additionally, Microsoft [also takes a portion][7] (30%) of any revenues generated from within the developer’s submitted application. When accounting for this dynamic, it becomes clear that _any_ attractive feature that the API/platform can provide to pull developers into this ecosystem (and by virtue its model) becomes tantamount, even if that means catering to developers whose skill set is better spent on a ubiquitous audience.

But even in this light, a web developer does not need to pay $19 for a ubiquitous application hosted on the web.  So, the incentive is further marginalized to cross the “backwards” WinJS bridge.

Finally, there’s another curious wrinkle to this strategy: Microsoft’s smart acceptance and promotion of web standards provides value in the form of goodwill to the industry and in mindshare, but it does not provide any direct revenues for the company’s bottom line.  As we have mentioned throughout this article, there is not a web client application model technology that is currently offered by Microsoft.  Instead, Microsoft expects its own client developers to use externally provided application models and solutions, such as [leveraging a curious relationship with Google][8] to support Angular for web client development.

Microsoft does not garner any revenues from this, and what’s more, Microsoft does not produce or retain any intellectual property or proffer any assets towards its intellectual property cache.  This leads to another confusing and seemingly self-inflicting question: why is Microsoft encouraging its own developers to use external, non-Microsoft technologies to build web-hosted client applications while simultaneously running a .NET client developer registration program whose purpose is to procure registrations (and revenues) for its Windows Store?  _For every Microsoft web developer out there deciding to deploy a ubiquitous web-hosted client application instead of deploying a client application to the Windows Store, Microsoft is losing $19 per developer_.

### Thinking Forward

Hopefully it is clear by now that Microsoft is offering guidance that not only hurts its developers and its brand, but is also offering a solution that simply flies backwards in the face of good business sense.  In our [next section][9], we aim to round out this series by demonstrating how Microsoft can fix these issues and mend their ecosystem by successfully creating and providing a ubiquitous .NET client application model offering.

### Show Your Support

If you like the idea of a ubiquitous .NET client application development model, please take the time and let Microsoft know by voting for this idea on UserVoice:

<div class="push-button-container"><div class="push-button">
</div><a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10027638-create-a-ubiquitous-net-client-application-develo" target="_blank"><div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;"></div><img class="push-button-vote-text" src="/images/VoteNow.svg" /></a></div>

 [1]: /2015/10/the-broken-burned-bridge/
 [2]: /2015/10/introduction/#who-are-you-who-is-the-8220we8221
 [3]: https://dev.windows.com/en-us/develop/winjs
 [4]: http://www.netmarketshare.com/report.aspx?qprid=10&qptimeframe=M&qpsp=198&qpch=350&qpmr=24&qpdt=1&qpct=3&qpcustomd=0&qpcid=fw829232&qpf=1
 [5]: https://github.com/MicrosoftEdge/JSBrowser
 [6]: https://dev.windows.com/en-us/Registration/AccountInfo
 [7]: http://www.windowscentral.com/microsoft-wants-bigger-cut-revenue-windows-developers
 [8]: http://blogs.msdn.com/b/somasegar/archive/2015/03/05/typescript-lt-3-angular.aspx
 [9]: /2015/10/the-ubiquitous-bridge/