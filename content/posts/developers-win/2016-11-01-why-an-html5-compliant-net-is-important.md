---
title: Why an HTML5-Compliant .NET is Important
author: Mike-EEE
type: post
date: 2016-11-01T17:33:33+00:00
excerpt: Exploring the cost considerations in developing a .NET application vs. a .NET paired with a JavaScript-based application.
url: /2016/11/why-an-html5-compliant-net-is-important/
mythemes-thumbnail-height:
  - 45
categories:
  - Developers-Win
  - General

---
### TL;DR: Vote!

<div class="push-button-container">
  <div class="push-button">
  </div>
  
  <a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10027638-create-a-ubiquitous-net-client-application-develo" target="_blank"> 
  
  <div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;">
  </div>
  
  <img class="push-button-vote-text" src="http://uploads.webflow.com/55e079ccd960e71226582014/55d09ab72123fb7e3e46b1cd_Vote%20Now!%20Text.svg" /></a>
</div>

### Exploring an HTML5-Compliant .NET

I recently got a <a href="http://forums.dotnetfoundation.org/t/cross-platform-wpf/421/109" target="_blank">good question on the .NET Foundation Forums </a>in regard to why I (<a href="https://visualstudio.uservoice.com/forums/121579-visual-studio-2015/suggestions/10027638-create-a-ubiquitous-net-client-application-develo" target="_blank">and nearly 5,200 other votes as of this writing</a>) feel so strongly about having an HTML5-compliant .NET (that is, a .NET runtime that runs within a browser process).  I attempted to answer the question <a href="http://forums.dotnetfoundation.org/t/cross-platform-wpf/421/110" target="_blank">here</a> and <a href="http://forums.dotnetfoundation.org/t/cross-platform-wpf/421/111" target="_blank">here</a>.  However, another point has emerged that has been nagging at me that I wanted to share.  So, rather than pollute the great thread there (seriously, do yourself a favor and <a href="http://forums.dotnetfoundation.org/t/cross-platform-wpf/421" target="_blank">read the entire thing</a>) with yet another post, I decided to make a quick post here instead.  Besides, I haven&#8217;t really posted here in a while and it is probably way past time to dust this thing off.

### Creating an Ubiquitous Application: Pre-Xamarin

Let&#8217;s say we want to create an application with maximum market reach, meaning we want it to reach as many devices as possible in today&#8217;s current marketplace.  At a minimum we will need:

  * Server (to host our APIs, services, and backend infrastructure code).
  * iOS native application
  * Droid native application
  * Windows native application
  * Website (really a web &#8220;application&#8221;)

Each of these require a codebase to operate.  Before the acquisition of Xamarin, to do this in .NET, you would use (with languages):

  * Server: .NET/C# (Serves 100% of the market of modern devices)
  * iOS: Objective-C (Roughly 50% of the market)
  * Droid: Java (Roughly 50% of the market)
  * Windows: .NET/C# (Roughly 30% of the market)
  * Web Application: JavaScript (100% of the market)

Let&#8217;s say for an entire year, each codebase within your solution would cost $100k &#8212; _per language used_.  This cost consideration is _**very rough estimate**_ from a small business perspective and includes:

  1. Acquiring the developer/resource necessary to code in that particular language
  2. The cost to develop the code
  3. The cost to maintain the code after it has been developed

Again this is _per language_ as each language _is incompatible and cannot be shared between the other_.  Using the setup above, we can combine the efforts in the Server and Windows as they both share the same language (.NET/C#) and can [_therefore share code between the two_][1].

So, our TCO breakdown would now look like (pivoting on technology used):

  * .NET/C#: ~$100k 
      * Server
      * Windows native application
  * Objective-C: ~$100k 
      * iOS native application
  * Java: ~$100k 
      * Droid native application
  * JavaScript: ~$100k 
      * Web application

**Estimated Total Annual Cost of Ownership: ~$400k**

### Post-Xamarin Acquisition

The above of course does not consider the Xamarin acquisition from last year.  Microsoft did the right thing here, not just from the technology perspective, but from the business and cost perspective.  Now our TCO breakdown looks like this when considering Xamarin in a .NET solution:

  * .NET/C#: ~$100k 
      * Server
      * iOS application (Xamarin)
      * Droid (Xamarin)
      * Windows native application (UWP)
  * JavaScript: ~$100k 
      * Web application

**Estimated Total Annual Cost of Ownership: ~$200k**

Getting better, right?  Well, it is.  _We have effectively halved our TCO_.  Good work, everybody, pat yourselves on the back!  However, we can do better, right?  As a savvy small business owner, we have to consider **all** possible options and _especially those that can save us even more money_.  If we now take the perspective of said business owner who is _technology-agnostic_ and not tied to a particular stack (read: has not drank the MSFT koolaid), we can now consider _maximizing our investment_ with any technology available that also attains our desired market reach.  This means comparing costs between .NET (above) and also JavaScript.  So, let&#8217;s compare the above with a JavaScript-based solution:

  * JavaScript: ~$100k 
      * Server (<a href="http://nodejs.org" target="_blank">NodeJS</a>)
      * iOS application (Cordova / <a href="http://searchcloudapplications.techtarget.com/podcast/NativeScript-framework-eases-cross-platform-app-development-woes" target="_blank">NativeScript</a> / <a href="https://www.smashingmagazine.com/2016/08/a-glimpse-into-the-future-with-react-native-for-web/" target="_blank">React Native</a>)
      * Droid application (Cordova / NativeScript / React Native)
      * Windows application (Cordova / NativeScript / React Native/ or even <a href="https://developer.microsoft.com/en-us/windows/bridges/hosted-web-apps" target="_blank">Windows Hosted Webapps</a>)
      * Web application (JavaScript&#8217;s/HTML5&#8217;s native environment, baby!)

**Estimated Total Annual Cost of Ownership: ~$100k (!)**

### It&#8217;s Just Business

So again, each of these $100k blocks are rough estimates, but you can now see we are dealing with a roughly **$200k .NET/JavaScript Annual TCO** vs. **$100k JavaScript Annual TCO**.  As a technology-agnostic small business owner who has a, say, $250k annual budget, which approach makes the most sense to you?

<div style="width: 510px" class="wp-caption alignnone">
  <a href="http://www.cc.com/shows/kroll-show" target="_blank"><img src="https://i1.sndcdn.com/artworks-000076719471-7rnumn-t500x500.jpg" alt="Good at Bizness" width="500" height="500" /></a>
  
  <p class="wp-caption-text">
    Good at Bizness
  </p>
</div>

 [1]: /2015/10/the-broken-burned-bridge/