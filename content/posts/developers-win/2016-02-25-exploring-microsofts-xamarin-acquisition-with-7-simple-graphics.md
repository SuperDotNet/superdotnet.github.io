---
title: Exploring Microsoft’s Xamarin Acquisition with 7 Simple Graphics
author: Mike-EEE
type: post
date: 2016-02-25T13:00:13+00:00
excerpt: "Now that Microsoft has acquired Xamarin, everything is great and we have cross-platform bliss, right?  Not so fast.  I explain why we shouldn't get so excited just yet."
url: /2016/02/exploring-microsofts-xamarin-acquisition-with-7-simple-graphics/
mythemes-thumbnail-height:
  - 45
dsq_thread_id:
  - 4610056765
categories:
  - Developers-Win
  - General

---
### TL;DR: Vote!

The purpose of this article is to build consensus around a ubiquitous .NET client application development model.  With Xamarin&#8217;s acquisition yesterday, this gets us closer, but not quite there.  Please show your support for a browser-hosted .NET runtime by voting for this issue in Visual Studio&#8217;s UserVoice here:

<div class="push-button-container"><div class="push-button">
</div><a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10027638-create-a-ubiquitous-net-client-application-develo" target="_blank"><div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;"></div><img class="push-button-vote-text" src="/images/VoteNow.svg" /></a></div>

### Xamarin is Acquired by Microsoft

<a href="http://weblogs.asp.net/scottgu/welcoming-the-xamarin-team-to-microsoft" target="_blank">Yesterday it was announced that Xamarin had been (finally) purchased by Microsoft</a>.  When I attended Evolve 2014 in Atlanta two Octobers ago, I had an absolute blast, and the running joke then was <a href="https://twitter.com/MikeEEE76/status/520701329527025665" target="_blank">that Xamarin is the new Microsoft</a> and that Microsoft should be concerned about Xamarin&#8217;s acquisition of _it_.  Well, we know now who is <a href="http://ytmnd.com" target="_blank">the bigger dog now</a> officially.  It now seems as if everyone is copacetically running in the same pack so that they can turn their eyes on the bigger alpha dog technology at the moment: <a href="https://nodejs.org/en/" target="_blank">NodeJS</a>.

### Setting the Stage: The Big Four

So why is NodeJS considered the &#8220;alpha dog technology&#8221;?  Why are <a href="/2016/02/the-net-to-nodejs-exodus-sound-off/" target="_blank">.NET developers ditching .NET and moving their code to Node</a>? Additionally, it now seems that we have cross-platform synchronicity with Xamarin and everyone is excited.  So what is the problem?

I will attempt to answer these questions in this article.  For the purposes of this discussion, I am going to approach it as if I am an ISV (<a href="https://en.wikipedia.org/wiki/Independent_software_vendor" target="_blank">independent software vendor</a> &#8212; ala someone who has not drank the MSFT Koolaid), and I want to build an application for today&#8217;s marketplace that ensures maximum market reach.  To do this, I am going to have to reach &#8220;The Big Four&#8221; marketplaces: Droid (approximately 1.7 billion devices), iOS (approximately 1 billion devices), Windows Store (approximately .5 billion devices), and the web (approximately 3 billion devices) (note: [please see how I got these numbers here][1]).  Or, as presented in a pretty picture (as pretty as I could make it, at least):

<div id="attachment_662" style="width: 1034px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2016/02/Big-Four.png" rel="attachment wp-att-662"><img class="wp-image-662 size-large" src="/wp-content/uploads/2016/02/Big-Four-1024x444.png" alt="The Big Four Platforms: Droid, iOS, Windows, and Web" width="1024" height="444" srcset="/wp-content/uploads/2016/02/Big-Four.png 1024w, /wp-content/uploads/2016/02/Big-Four-300x130.png 300w, /wp-content/uploads/2016/02/Big-Four-768x333.png 768w" sizes="(max-width: 1024px) 100vw, 1024px" /></a>
  
  <p class="wp-caption-text">
    The Big Four Platforms: Droid, iOS, Windows, and Web
  </p>
</div>

### Reaching The Big Four with .NET

With Xamarin&#8217;s acquisition, <a href="http://mspoweruser.com/xamarin-deal-may-bring-universal-windows-apps-to-ios-and-android/" target="_blank">developers are already anticipating a cross-platform Universal Windows Platform</a> &#8212; and they should.  In fact, at this point, if something along these lines is _not_ announced at <a href="http://build.microsoft.com/" target="_blank">//build</a> or <a href="http://evolve.xamarin.com" target="_blank">Evolve</a>, it will be a disappointment.  Now, let&#8217;s imagine that there _is_ a new UWP platform &#8212; let&#8217;s call it the **Multiversal .NET Platform** &#8212; that is built with the new Xamarin acquisition, and I as an ISV want to reach The Big Four.  This is what it would look like from a hypothetical Multiversal .NET perspective, now enabled by Xamarin:

<div id="attachment_666" style="width: 1034px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2016/02/MultiversaldotNET.png" rel="attachment wp-att-666"><img class="size-large wp-image-666" src="/wp-content/uploads/2016/02/MultiversaldotNET-1024x512.png" alt="Multiversal .NET via Xamarin" width="1024" height="512" srcset="/wp-content/uploads/2016/02/MultiversaldotNET.png 1024w, /wp-content/uploads/2016/02/MultiversaldotNET-300x150.png 300w, /wp-content/uploads/2016/02/MultiversaldotNET-768x384.png 768w" sizes="(max-width: 1024px) 100vw, 1024px" /></a>
  
  <p class="wp-caption-text">
    Multiversal .NET via Xamarin
  </p>
</div>

Notice something?  All of the Big Four _with the exception of the web_ are accounted for in this new paradigm.  What&#8217;s the big deal, you ask?  [NodeJS is even endorsed by Microsoft to build web applications][2].  Let&#8217;s explore that further.

### Reaching The Big Four with NodeJS

Remember, _I am thinking from an ISV perspective_.  I want to maximize my market reach, eliminate risks, and lower my <a href="https://en.wikipedia.org/wiki/Total_cost_of_ownership" target="_blank">total cost of ownership</a> as much as possible.  I will look at Microsoft&#8217;s guidance above and say &#8220;Hey you know what, Microsoft?  This NodeJS you mention is a good idea.  _Thanks for suggesting it!_  In fact, when I use it with <a href="https://cordova.apache.org/" target="_blank">Cordova</a>, I can also reach the other native platforms and _save money by only having to use one technology, one language, and therefore one code base to reach all my desired scenarios_.&#8221;  That is seen here:

<div id="attachment_667" style="width: 1034px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2016/02/Node.png" rel="attachment wp-att-667"><img class="size-large wp-image-667" src="/wp-content/uploads/2016/02/Node-1024x512.png" alt="Node.js Platform Reach When Paired with Cordova" width="1024" height="512" srcset="/wp-content/uploads/2016/02/Node.png 1024w, /wp-content/uploads/2016/02/Node-300x150.png 300w, /wp-content/uploads/2016/02/Node-768x384.png 768w" sizes="(max-width: 1024px) 100vw, 1024px" /></a>
  
  <p class="wp-caption-text">
    Node.js Platform Reach When Paired with Cordova
  </p>
</div>

You now might be asking&#8230; _hey, what happened to .NET_?  Where did it go?

<div style="width: 370px" class="wp-caption aligncenter">
  <a href="http://www.reactiongifs.us/wp-content/uploads/2014/10/aha_coming_to_america.gif"><img class="" src="http://www.reactiongifs.us/wp-content/uploads/2014/10/aha_coming_to_america.gif" alt=".NET Go Bye-Bye" width="360" height="200" /></a>
  
  <p class="wp-caption-text">
    .NET Go Bye-Bye
  </p>
</div>

### The Three Major Hosted Scenarios

So far we have been talking client-side hosting scenarios.  What we haven&#8217;t been talking about &#8212; and is <a href="http://azure.microsoft.com" target="_blank">already solved quite convincingly by Microsoft</a> &#8212; is the server-side scenario.  **Remember, the more code you have within your code base, the higher the TCO**, so you want to [encapsulate and share code as much as possible whenever you can][3], reducing the amount of duplicated code &#8212; and the amount of code in general.  This was the major benefit of [Silverlight][4] back in the day, and as we will see, the major benefit now when using NodeJS.

To start, here are our hosted scenarios, and the code required to run them:

<div id="attachment_669" style="width: 1002px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2016/02/HostedScenarios.png" rel="attachment wp-att-669"><img class="size-full wp-image-669" src="/wp-content/uploads/2016/02/HostedScenarios.png" alt="Hosted Scenarios" width="992" height="374" srcset="/wp-content/uploads/2016/02/HostedScenarios.png 992w, /wp-content/uploads/2016/02/HostedScenarios-300x113.png 300w, /wp-content/uploads/2016/02/HostedScenarios-768x290.png 768w" sizes="(max-width: 992px) 100vw, 992px" /></a>
  
  <p class="wp-caption-text">
    Hosted Scenarios
  </p>
</div>

### Hosted Scenarios with NodeJS

Below you can see what these hosted scenarios look like when using NodeJS.  I have color-coded the areas where you can share code between the scenarios.  The middle is where code reuse is maximized between all hosted scenarios, and therefore enjoys the greatest TCO efficiency and therefore <a href="http://www.investopedia.com/terms/r/returnoninvestment.asp" target="_blank">ROI</a>.

<div id="attachment_670" style="width: 677px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2016/02/HostedScenariosNodeJS.png" rel="attachment wp-att-670"><img class="size-full wp-image-670" src="/wp-content/uploads/2016/02/HostedScenariosNodeJS.png" alt="Code Reuse Between Hosted Scenarios with NodeJS" width="667" height="631" srcset="/wp-content/uploads/2016/02/HostedScenariosNodeJS.png 667w, /wp-content/uploads/2016/02/HostedScenariosNodeJS-300x284.png 300w" sizes="(max-width: 667px) 100vw, 667px" /></a>
  
  <p class="wp-caption-text">
    Code Reuse Between Hosted Scenarios with NodeJS
  </p>
</div>

### Hosted Scenarios with Multiversal .NET using Xamarin

Here we see the same with .NET.  Notice we cannot share code with the browser scenarios because it is written in JavaScript/NodeJS and therefore completely incompatible with any .NET client application model.

<div id="attachment_671" style="width: 946px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2016/02/HostedScenariosNet.png" rel="attachment wp-att-671"><img class="size-full wp-image-671" src="/wp-content/uploads/2016/02/HostedScenariosNet.png" alt="Code Reuse Between Hosted Scenarios with Multiversal .NET" width="936" height="600" srcset="/wp-content/uploads/2016/02/HostedScenariosNet.png 936w, /wp-content/uploads/2016/02/HostedScenariosNet-300x192.png 300w, /wp-content/uploads/2016/02/HostedScenariosNet-768x492.png 768w" sizes="(max-width: 936px) 100vw, 936px" /></a>
  
  <p class="wp-caption-text">
    Code Reuse Between Hosted Scenarios with Multiversal .NET
  </p>
</div>

### Show Your Support

Hopefully this makes a little more sense to the casual observer.  The purpose of this article (and site) is to build consensus around the idea of a ubiquitous .NET client application development model offering.  With Xamarin&#8217;s acquisition yesterday, we are much closer to this goal, but not entirely there yet.  Please show your support for this by telling Microsoft you would like to see support for this by voting for this idea here:

<div class="push-button-container"><div class="push-button">
</div><a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10027638-create-a-ubiquitous-net-client-application-develo" target="_blank"><div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;"></div><img class="push-button-vote-text" src="/images/VoteNow.svg" /></a></div>

Thank you all as always for reading, your feedback, and support!

&nbsp;

 [1]: /2016/02/how-nodejs-is-dominating-net-in-3-easy-charts/#platform-market-reach
 [2]: /2015/12/is-net-in-trouble-belated-thoughts-from-connect-2015/
 [3]: /2015/10/the-broken-burned-bridge/
 [4]: /2015/10/existing-net-client-application-models/#silverlight