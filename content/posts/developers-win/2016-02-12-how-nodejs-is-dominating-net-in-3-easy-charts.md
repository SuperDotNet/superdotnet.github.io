---
title: How NodeJS Is Dominating .NET in 3 Easy Charts
author: Mike-EEE
type: post
date: 2016-02-12T12:38:24+00:00
excerpt: In this article, I take a quick visual look at how NodeJS is winning the developer war against Microsoft through the use of 3 simple charts.
url: /2016/02/how-nodejs-is-dominating-net-in-3-easy-charts/
mythemes-thumbnail-height:
  - 45
dsq_thread_id:
  - 4573260137
categories:
  - Developers-Win
  - General

---
### <a href="http://i.imgur.com/AxtzziK.gif" target="_blank">Wat</a> Now?

OK I have to admit my title to this article is my first attempt at click bait.  Hey, I&#8217;m learning my new toy here, what can I say?  But, I think what you&#8217;ll find in this article will be of value to you if you are a .NET developer (or an application or web developer with any sort of business acumen).

In this article, I am going to put a little more thought into a concept that have touched on and by accounts have assumed readers might already understand.  I am going to dive into it a little more to make sure that I have this stated and also provide an opportunity for those to offer their feedback (welcomed &#8212; as always!) to correct any assumptions (to assume does indeed make an &#8220;ass of u and me&#8221; &#8212; but mostly me in this case) that I have.

In doing so, I hope this will help others understand the driving business force and factors for Microsoft **<a href="http://visualstudio.uservoice.com/forums/121579-visual-studio-2015/suggestions/10027638-create-a-ubiquitous-net-client-application-develo" target="_blank">to provide a ubiquitous .NET client application development model offering</a>**.

<div class="push-button-container">
  <div class="push-button">
  </div>
  
  <a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10027638-create-a-ubiquitous-net-client-application-develo" target="_blank"> 
  
  <div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;">
  </div>
  
  <img class="push-button-vote-text" src="http://uploads.webflow.com/55e079ccd960e71226582014/55d09ab72123fb7e3e46b1cd_Vote%20Now!%20Text.svg" /></a>
</div>

### Platform Market Reach

To start with, I am going to give an overview of the big three players: Microsoft (around which my 15-year career and consequently this blog is built around), Apple, and Google.  Here I have made a chart with the awesome <a href="https://live.amcharts.com/" target="_blank">amCharts</a> showing the three platforms as they currently stand to my knowledge in the marketplace:



First, if you are wondering about the colors, I attempted to find a color from each store&#8217;s logo and use it accordingly.

Secondly (and more importantly), _how did I get these numbers_?  To be fair, they are all guestimates.  I do not have the quoted $6-10k (!) required from <a href="http://www.netmarketshare.com/" target="_blank">NetMarketShare</a> to get exact numbers that an analyst will have to work a few weeks to figure out.  However, I can extrapolate from data that I have seen around the interwebs. To start with, <a href="http://www.theverge.com/2016/1/26/10835748/apple-devices-active-1-billion-iphone-ipad-ios" target="_blank">if Apple currently has 1 billion active devices</a>, and <a href="http://www.netmarketshare.com/report.aspx?qprid=8&qptimeframe=M&qpsp=204&qpch=350&qpmr=100&qpdt=1&qpct=3&qpcustomd=1&qpcid=fw640619&qpf=1" target="_blank">Apple has ~33% of the market</a>, that means <a href="http://www.netmarketshare.com/report.aspx?qprid=8&qptimeframe=M&qpsp=204&qpch=350&qpmr=100&qpdt=1&qpct=3&qpcustomd=1&qpcid=fw640619&qpf=1" target="_blank">if Droid has ~59% of the market</a>, then Google Play has around 1.7 billion devices.  Additionally, if <a href="https://blogs.windows.com/windowsexperience/2016/01/04/windows-10-now-active-on-over-200-million-devices/" target="_blank">Windows 10 has 200 million installs</a>, and <a href="http://www.netmarketshare.com/report.aspx?qprid=10&qptimeframe=M&qpsp=204&qpch=350&qpmr=24&qpdt=1&qpct=3&qpcustomd=0&qpcid=fw216991&qpf=1" target="_blank">Windows 10 has ~12% of the market</a>, then I can extrapolate the numbers for Windows 7 at ~52% (885.5 million &#8211; !), Windows 8 at ~3% (45 million) and Windows 8.1 at ~10% (175.5 million).

Make sense?  Please let me know in the comments below if I am way off base here in some way and I will adjust accordingly.

### Native-Hosted Technology Reach

With our platform market reach ascertained, we can start to break down the relevant different technologies available to .NET developers, and see how they stack up.  I will start first by way of native-hosted client application technologies.  These are technologies that are run within a host of a native platform process (like a store or OS).  For a .NET developer, the following options are available to them:

  * [Universal Windows Platform][1] (Windows Store-capable OS&#8217;s, so Windows 8+)
  * [Windows Presentation Foundation][2] (.NET 4.5+, so Windows 7+)
  * <a href="https://developer.xamarin.com/api/root/ios-unified/" target="_blank">Xamarin.iOS</a> (Apple Store)
  * <a href="https://developer.xamarin.com/api/root/MonoAndroid-lib/" target="_blank">Xamarin.Android</a> (Google Play)
  * <a href="/2015/10/existing-net-client-application-models/#xamarinforms" target="_blank">Xamarin.Forms</a> (Windows Store, Apple Store, Google Play)
  * <a href="https://www.visualstudio.com/en-us/features/node-js-vs.aspx" target="_blank">NodeJS</a> with <a href="https://www.visualstudio.com/en-us/features/cordova-vs.aspx" target="_blank">Cordova</a> (Windows Store, Apple Store, Google Play)



From the looks of this, a .NET developer might be tempted to go with Xamarin.Forms, which is understandable.  However, as we can see, NodeJS gets as much reach as Xamarin.Forms.  Let&#8217;s also remember that from an ISV perspective, [Xamarin.Forms is a 3rd-party product and not a first-class promoted and supported technology like UWP is][3].  Additionally, we also have a _**very**_ significant scenario to consider: web-hosted applications.

### Web-Hosted Technology Reach

Now I am going to take the same technologies available to .NET developers as listed above and chart them out as they are available to web-hosted application development.  In this case, a web-hosted application is an application that lives within a web-host &#8212; or to be more precise, **an HTML5-compliant browser**.



Notice something?  **Not a single available recommended .NET technology offering works within a web-hosted environment with the exception of NodeJS** &#8212; _which is not even a Microsoft technology_!  In fact, instead of creating a competitive .NET model to NodeJS, [Microsoft leadership is inexplicably pushing its developers to use NodeJS on the client and .NET on the server][4], which will [only create costly and inefficient solutions][5] &#8212; which in turn will _[eventually push every .NET developer to NodeJS!][6]_  Well, those who care about writing cost-effective and efficient solutions, that is.

### NodeJS Dominance

To wrap up here, NodeJS:

  * Works in Native-hosted application scenarios (via Cordova), reaching _over approximately 3 billion devices_.
  * Works in Web-hosted application scenarios, again reaching _over approximately 3 billion devices and workstations_.
  * _Works in server-process-hosted scenarios and therefore (most importantly)_
  * **Saves [money and resources][7] by allowing code reuse between server and client, [preserving encapsulation and honoring DRY][8].**

It is no wonder <a href="/2016/02/the-net-to-nodejs-exodus-sound-off/" target="_blank">that .NET developers are starting to gravitate over to NodeJS and ditching .NET altogether</a>.  I personally have to be honest here and say that the more I talk about this subject, the more I am convincing myself to do the exact same thing!  However, it is hard to give up 15 years of investment (I still have faith!), and that is why I am promoting the following vote.

### Show Your Support

If you like the idea of a ubiquitous .NET client application development model offering from Microsoft, please take the time and let Microsoft know by voting for this idea on UserVoice by clicking the pretty button here and voting on the issue there:

<div class="push-button-container">
  <div class="push-button">
  </div>
  
  <a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10027638-create-a-ubiquitous-net-client-application-develo" target="_blank"> 
  
  <div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;">
  </div>
  
  <img class="push-button-vote-text" src="http://uploads.webflow.com/55e079ccd960e71226582014/55d09ab72123fb7e3e46b1cd_Vote%20Now!%20Text.svg" /></a>
</div>

Thank you all as always for reading, your feedback, and support!

 [1]: /2015/10/existing-net-client-application-models/#universal-windows-platform
 [2]: /2015/10/existing-net-client-application-models/#windows-presentation-foundation
 [3]: /2016/02/the-backwards-windows-platform-bridges-the-business-problem/#what-about-xamarin
 [4]: /2015/12/is-net-in-trouble-belated-thoughts-from-connect-2015/
 [5]: /2016/02/the-great-net-client-divide-a-simple-example-hopefully/
 [6]: /2016/02/the-net-to-nodejs-exodus-sound-off/
 [7]: /2015/10/the-broken-burned-bridge/#organizational-and-resource-problem
 [8]: /2015/10/the-broken-burned-bridge/#conceptual-and-architectural-problem