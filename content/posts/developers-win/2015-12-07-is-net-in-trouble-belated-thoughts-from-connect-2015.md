---
title: 'Is .NET in Trouble?  (Belated Thoughts from Connect 2015)'
author: Mike-EEE
type: post
date: 2015-12-07T14:30:09+00:00
excerpt: "This article explores Microsoft's endorsed strategy from Connect 2015, and shows how it ultimately harms the .NET brand -- by forcing organizations that follow it to create a culture of .NET generalists rather than .NET experts."
url: /2015/12/is-net-in-trouble-belated-thoughts-from-connect-2015/
featured_image: /wp-content/uploads/2015/12/GeneralistVsExperts.png
mythemes-thumbnail-height:
  - 45
dsq_thread_id:
  - 4378205156
categories:
  - Developers-Win
  - General

---
### TL;DR: VOTE!

This post exists to build consensus in the Microsoft developer community around the idea of a ubiquitous .NET client application development model.  Show your support by voting for this idea here:

<div class="push-button-container">
  <div class="push-button">
  </div>
  
  <a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10027638-create-a-ubiquitous-net-client-application-develo" target="_blank"> 
  
  <div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;">
  </div>
  
  <img class="push-button-vote-text" src="http://uploads.webflow.com/55e079ccd960e71226582014/55d09ab72123fb7e3e46b1cd_Vote%20Now!%20Text.svg" /></a>
</div>

## &#8220;But Connect 2015 was over Two Weeks Ago!&#8221;

Developers.win is a personal passion project of mine, so it is at the mercy of my schedule, whenever I can find time for it.  Case in point, I am just now getting to write this post, which is essentially my thoughts on Connect 2015, an event that occurred over two weeks ago.  Of course, schedule and time are relative, as this post is actually driven by great conversations held in the <a href="https://disqus.com/" target="_blank">Disqus</a> comments in <a href="http://microsoft-news.com/" target="_blank">Microsoft News</a>.  Somehow, I found the time to have those, and in doing so I kept thinking to myself, &#8220;why not make a blog post over this?&#8221;  So, I put it on my task list for when I can get to it, and here we are.

(For those who are interested for the discussions inspiring this post, check out <a href="http://microsoft-news.com/google-engineer-we-share-the-same-soul-with-microsoft/" target="_blank">this article</a> and <a href="http://microsoft-news.com/google-play-music-now-has-an-unofficial-app-for-windows/" target="_blank">this article</a> , skipping straight to the comments &#8212; there the true content of any worthy article posted these days truly lies.)

## The Problem

[We have already seen the error in the technical advice given by the Visual Studio group in regards to its &#8220;answer&#8221; to Silverlight 6][1].  Unfortunately, this same &#8220;strategic&#8221; thinking (for whatever reason) still permeates Microsoft today and was on full display during Connect 2015.

While on stage during Connect 2015, Scott Hanselman, Scott Guthrie, and Anders Hejlsberg all happily endorsed Visual Studio solutions featuring a JavaScript (and TypeScript) client running on top of a .NET back end.  This is (and really has been) considered the &#8220;new&#8221; de-facto standard for any &#8220;.NET development&#8221; for the new world of ASP.NET 5 and the new .NET Core (or is that Core .NET?  I always get those confused&#8230; let me go look it up **again** to make sure&#8230;).

Not many .NET developers have questioned this approach, which I find disturbing from a .NET perspective and hence the driving force behind this article.  To be sure, Microsoft is reaching out its olive branch to non-.NET (read: <a href="https://nodejs.org/en/" target="_blank">Node.js</a>) developers to provide offerings to entice them and bring them into their platforms, most notably Azure and the new Visual Studio Team Services, which were clearly the star of the Connect 2015 show.

My guess is that .NET developers &#8212; like all developers &#8212; have been mesmerized (dumbfounded, even) by Microsoft&#8217;s new approach and shocking shift to embracing open source and cross-platform technologies.  However, .NET developers have not really given much thought to HOW (or in particular _the strategy_) Microsoft is doing so.

_Microsoft should indeed be reaching out and enticing non-MSFT developers into its technologies and platforms, **but not at the expense of .NET and its traditional application development offerings**._

## Building a Culture of Excellence (Experts) over Mediocrity (Generalists)

I&#8217;m going to take a step back and try to explore the root of the problem here as I see it.  I am hoping that once the root is explored, the flaw in Microsoft&#8217;s current application development endorsement will be easier to see.

Let&#8217;s start with our good friend Malcolm Gladwell (he IS your good friend, right?) and his 10,000 hour rule.  <a href="http://www.businessinsider.com/malcolm-gladwell-explains-the-10000-hour-rule-2014-6" target="_blank">Here is a good article that even explains how it is completely used wrong and misused by everyone</a>.  For the purposes of this article, I simply want to use the 10,000 hour metric as a way to identify an &#8220;expert&#8221; within a system, or more specifically an organization.

An expert within a system is more cost effective within an organization as they have a valuable combination of talent and experience.  They understand a particular system (domain) and its idiosyncrasies.  They know all the tricks, but more importantly, since they also have the talent, they are constantly innovating within their field of expertise.  From a business perspective, experts are cost effective to an organization as their skill set can be leveraged with more efficiency than those of generalists (non-experts).  _This is because experts typically can get a job done faster and at a higher quality than generalists._

Generalists (non-experts) are more expensive to an organization as they do not completely understand the problem domain as well as an expert.  In software development, this leads to lower quality product (code) as the product tends to have more defects due to poorer design (deficient knowledge).  Generalists do not fully understand the idiosyncrasies of the system, and this leads to inefficient use of the system to yield desired results.

Since generalists are not as knowledgeable about a system, they take longer to work with it.  In software development, this manifests in inaccurate estimates and longer development times for tasks that could (typically) be better-designed and develop by an expert &#8212; with a (typically) lower defect count.

Then there is the issue of financial cost.  Let&#8217;s say that I am a business owner that wants an app built.  If I am presented with the option of hiring two generalists (lower rate) or one expert (higher rate), I will be tempted to choose the expert as that is less resources spent on management (one resource rather than two), while getting a higher quality code base (and resulting product) that is developed faster (high system knowledge) than a generalist (general system knowledge).

## &#8220;Full-Stack&#8221; &#8220;Expert&#8221;

This (hopefully) brings us back to the main point of the discussion.  I see a lot of job listings out there for a &#8220;full-stack&#8221; developer, and what these listings really mean is that they want a developer that can code from user interface all the way to the database.  This, of course, requires knowledge in different technologies, and these listings seem to pride themselves on naming as many technologies as possible.  Unless they land a very rare developer who has spent 10,000 hours on each of those technologies, what the company ultimately ends up with is a  generalist that can &#8220;wear many hats&#8221; and is a &#8220;jack of all trades&#8221; (and indeed, is a master of none).

Now, I will admit that I get a case of _schadenfreude_ when I see these requirements as I know what sort of dumpster fire is currently sitting in their source control.  The reason (or one of many reasons) why their code is always on fire (and they are constantly firing and hiring a new fire marshal) is that these organizations continue to seek and hire generalists to build upon on their solutions that span these many different technologies.  This is a very messy and error-prone way of handling solution development, and anyone who has had to endure such a scenario &#8212; since there are always so many of these listings we can assume that a large majority of the developer population has been recycled through one or two of these &#8212; can attest to this madness.

Now consider a &#8220;full stack&#8221; solution where the same web-hosted (ubiquitous) technology is used from user interface to database.  If you are a .NET developer, <a href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10027638-create-a-ubiquitous-net-client-application-develo" target="_blank">you will have to close your eyes and imagine a world like this at the present moment</a>.  _However, if you are lucky enough to be a Node.js developer, you don&#8217;t have to do much imagining, as you are living it._

As a Node.js developer, you enjoy access to a viable <a href="http://adrianmejia.com/blog/2014/09/28/angularjs-tutorial-for-beginners-with-nodejs-expressjs-and-mongodb/" target="_blank">JavaScript-based API for client-side development</a>, <a href="https://scotch.io/tutorials/build-a-restful-api-using-node-and-express-4" target="_blank">service/service-based development</a>, and <a href="https://www.npmjs.com/package/sql" target="_blank">database-based development</a> (full disclosure: I am not a Node.js developer, I just like to Google about it when I am writing a blog article about it).  As a result, every second spent within a Node.js solution built in this system is one second closer to becoming a 10,000-hour Node.js/JavaScript/TypeScript expert.

Conversely, as a .NET &#8220;web&#8221; developer, you have to spend your time between C#/.NET on the server side, T-SQL on the database (unless you use an O/R mapping solution like <a href="https://github.com/aspnet/EntityFramework" target="_blank">EntityFramework</a> &#8212; or _gasp_ use T-SQL right in your C#: YUCK!), and &#8212; SURPRISE! &#8212; Node.js (and/or Angular.js) on the client-side.  This is because &#8212; _as we saw on full display in Connect 2015_ &#8212; Microsoft is not offering a web client development solution, but is inexplicably leaning on Google to provide it for them.  Spending 10,000 hours across these two (or three) different technology offerings does not an expert make in a single one of these areas.

<div id="attachment_502" style="width: 763px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2015/12/GeneralistVsExperts2.png"><img class="wp-image-502" src="/wp-content/uploads/2015/12/GeneralistVsExperts2.png" alt="Showcasing the difference between .NET and Node.js web development after 10,000 of development time." width="753" height="343" /></a>
  
  <p class="wp-caption-text">
    Showcasing the difference between .NET and JavaScript (Node.js) web development after 10,000 hours of development time.
  </p>
</div>

<span style="color: #ff0000;"><em><strong>As a result, Node.js application development is successfully producing &#8220;full-stack&#8221; experts in Node.js and JavaScript, whereas .NET application development is producing &#8220;full-stack&#8221; generalists in .NET (and maybe even Sql Server) and Node.js.</strong></em></span>

## Flocking to Node.js

The additional problem here is obviously that I am not alone in seeing this, and companies/organizations are catching on to this as well.  <a href="http://forums.dotnetfoundation.org/t/cross-platform-wpf/421/71" target="_blank">You are starting to see chatter online in developers</a> and their organizations realize the benefits of having a single technology and language used &#8220;full stack&#8221; from client to database.  Why use .NET when it gets in the way and is ultimately not like the JavaScript that is used in the client?  Why use .NET when you can&#8217;t use that fancy new ExceptionReporter (or is that _exceptionReporter_? ha ha &#8212; [different casing in JavaScript][2], right&#8230; RIGHT?!) you made in JavaScript, but can use it within a Node.js server boundary?

Ultimately, as a .NET web developer that Microsoft is endorsing in Connect 2015, you are having to build and maintain two different code bases (.NET and JavaScript/TypeScript), and that is ultimately _expensive_ both from a technical and human resource point of view.  I hope this is obvious why:

  * Each code base has its own set of defects.
  * Each code base has its own set of class definitions and concerns (that may or may not overlap each other).
  * Each code base requires a skill set to build and maintain, which may or may not be possible to address with one person. 
      * Even if one person can manage each code base, they may not be an expert in both of them. This affects quality (and therefore Total Cost of Ownership).

## Stemming the Flow

So what to do?  Developers.win is committed to building consensus around the concept of a ubiquitous .NET client application development model within Microsoft and its community of developers.  The only power we have as Microsoft developers is to use UserVoice to show that we want this addressed.  Microsoft does use and pay attention to its UserVoice, so please, take a second to vote with the pretty vote button below.  Also, please feel free to leave a comment as well, as this is my baby and I am very interested in hearing what other developers think about it.  Thank you for your consideration and support!

<div class="push-button-container">
  <div class="push-button">
  </div>
  
  <a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10027638-create-a-ubiquitous-net-client-application-develo" target="_blank"> 
  
  <div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;">
  </div>
  
  <img class="push-button-vote-text" src="http://uploads.webflow.com/55e079ccd960e71226582014/55d09ab72123fb7e3e46b1cd_Vote%20Now!%20Text.svg" /></a>
</div>

 [1]: /2015/10/the-broken-burned-bridge/
 [2]: /2015/10/ubiquitous-qualities/#holistic-development-consistency