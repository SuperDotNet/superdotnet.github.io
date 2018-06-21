---
title: Is the Tide Turning on project.json?
author: Mike-EEE
type: post
date: 2016-02-11T13:52:22+00:00
url: /2016/02/has-the-tide-turned-on-project-json/
mythemes-thumbnail-height:
  - 45
dsq_thread_id:
  - 4570417616
categories:
  - Developers-Win
  - General

---
### <a href="https://i.ytimg.com/vi/1IkGj5Ghgm4/hqdefault.jpg" target="_blank">Wat</a> Want?

I am not exactly a fan of the new project.json initiative underway between the Visual Studio and ASP.NET Core rewrite.  In fact, I have been so concerned with it that **<a href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/9347001-improve-reboot-visual-studio-project-system" target="_blank">I have created a vote to change this very issue along with other latent misgivings in the Visual Studio project system</a>**.

### <a href="http://littlefun.org/uploads/521121d3c856117929000000_736.jpg" target="_blank">Wat</a> Wrong?

<a href="http://stackoverflow.com/questions/244777/can-i-use-comments-inside-a-json-file" target="_blank">The JSON specification simply does not support comments within its documents</a>, a fact (read: oversight) that seems to have escaped the ASP.NET Core team in their analysis of JSON the format of choice to serialize their new project initiative.

### So&#8230; <a href="http://i.imgur.com/AxtzziK.gif" target="_blank">Wat</a>?

Recently someone posted <a href="https://twitter.com/joewalnes/status/696765701059670016" target="_blank">a very sane and reality-based Tweet stating that JSON files should NOT be used for configuration, schemas, etc</a>. Hallelujah!  I am not some mad man wandering alone in this wilderness after all.

###  Xml?

In response to that tweet, other <a href="https://twitter.com/mkristensen/status/696767036559503360" target="_blank">MSFT developers have jumped in and have tried to defend the questionable</a> &#8212; and inexplicable from the Microsoft IP perspective, as I explain in a bit &#8212; decision to pursue JSON over other formats.  In fact, a good number of developers (<a href="http://developers.win/visualstudio" target="_blank">as you can see from the vote I am promoting here</a>) prefer other formats such as <a href="https://twitter.com/ploeh/status/697309003936882688" target="_blank">XML, the mature serialization technology</a> to represent their data.

Now, there are many data formats out there, and [that is something that should definitely be accounted for in future versions of tooling][1].  However, none of these formats are as powerful _and native_ to Microsoft developers as Xaml.

### XAML?!

Yes, Xaml. A **Microsoft-**created, supported, and mature _serialization and object-description_ language used in basically every major Microsoft group with the exception of &#8230; well, ASP.NET and <a href="https://github.com/dotnet/corefx/issues/5766" target="_blank">.NET Core</a>.  To start with here, Xaml stands for eXtensible _**Application**_ Markup Language.  Why, from the sounds of it, defining a new project structure is perfect for this!  In fact, you can define an _entire application_ in Xaml if you are so inclined (see: the **A** in X**a**ml).  Xaml can be used to describe **any** _<a href="https://en.wikipedia.org/wiki/Plain_Old_CLR_Object" target="_blank">POCO</a>_ you wish, not just user interface elements.

<div id="attachment_612" style="width: 500px" class="wp-caption aligncenter">
  <img class="size-full wp-image-612" src="/wp-content/uploads/2016/02/h6ho21.jpg" alt="The moment you realize you can use Xaml for more than just User Interfaces" width="490" height="266" srcset="/wp-content/uploads/2016/02/h6ho21.jpg 490w, /wp-content/uploads/2016/02/h6ho21-300x163.jpg 300w" sizes="(max-width: 490px) 100vw, 490px" />
  
  <p class="wp-caption-text">
    The moment you realize you can use Xaml for more than just User Interfaces
  </p>
</div>

As any example, you can see this screenshot of the <a href="https://github.com/DevelopersWin/VoteReporter" target="_blank">Console Application</a> &#8212; yes, _a_ _**<a href="https://github.com/DevelopersWin/VoteReporter" target="_blank">Console Application</a>** described in **<a href="https://github.com/DevelopersWin/VoteReporter/blob/master/DevelopersWin.VoteReporter.Application/Program.xaml" target="_blank">Xaml</a>**_ &#8212;  that is used here at <a href="http://developers.win" target="_blank">Developer Wins!</a> to build [the weekly vote reports deployed every Friday morning][2]:

<div id="attachment_613" style="width: 310px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2016/02/2016-02-11_06221.png"><img class="wp-image-613 size-medium" src="/wp-content/uploads/2016/02/2016-02-11_06221-300x139.png" alt="Xaml-Described Console Application" width="300" height="139" srcset="/wp-content/uploads/2016/02/2016-02-11_06221-300x139.png 300w, /wp-content/uploads/2016/02/2016-02-11_06221-768x355.png 768w, /wp-content/uploads/2016/02/2016-02-11_06221-1024x473.png 1024w" sizes="(max-width: 300px) 100vw, 300px" /></a>
  
  <p class="wp-caption-text">
    Xaml-Described Console Application
  </p>
</div>

It is a small jump from here to see that Xaml can be used to support a new project structure altogether (and the effort would be minimal, considering the vast resources that have been placed in the new project.json structure already).  _Again, the tooling is already in place and is mature._

To summarize, Xaml is:

  * An eXtensible **Application** Markup Language (bears repeating)
  * Class-driven schema model (no need to create &#8220;yet another artifact&#8221; to describe the item you are describing &#8212; the class that you have **already created** _is_ the schema.)
  * Extremely powerful serialization model
  * **_A Microsoft property and invention_**
  * Designer-friendly
  * Mature (nearly a decade old)

### Value IP (Intellectual Property)

Much like how the [Windows Platform group is harming the value of its owns developers by building a backwards bridge from iOS into Windows][3], the ASP.NET Core group is ultimately harming Microsoft&#8217;s IP portfolio by choosing another external document format standard over one that already works within its technological capabilities.  Don&#8217;t get me wrong (too late, I know, haha!), I am all for adopting open standards, and the ASP.NET group &#8212; along with the Edge group &#8212; _have done a remarkable job in doing just that_.  However, in this case, this certainly requires some additional review and consideration, especially when the way that they are <a href="http://stackoverflow.com/questions/244777/can-i-use-comments-inside-a-json-file" target="_blank">utilizing a document format is violating the very standards they are trying to uphold</a>.

### Scheduling and Effort

Finally, the last consideration here is scheduling and effort.  Look at all the effort being placed into this new project system and the serious overlap of existing functionality with existing MSBuild and *proj files.  Look at all the effort put into the new tooling for intellisense and schema.  If Xaml was leveraged instead, minimal effort would have been put into update the tooling to play with the new bits (this is talking from the Visual Studio IDE and not Visual Studio Code perspective), and <a href="https://blogs.msdn.microsoft.com/webdev/2016/02/01/an-update-on-asp-net-core-and-net-core/" target="_blank">we would probably get less blog posts about how schedules are slipping</a>.

### Show Your Support

If you agree with me and would like to see Microsoft reconsider its current path in its project.json initiative, please show your support here:

<div class="push-button-container">
  <div class="push-button">
  </div>
  
  <a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/9347001-improve-reboot-visual-studio-project-system" target="_blank"> 
  
  <div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;">
  </div>
  
  <img class="push-button-vote-text" src="http://uploads.webflow.com/55e079ccd960e71226582014/55d09ab72123fb7e3e46b1cd_Vote%20Now!%20Text.svg" /></a>
</div>

 [1]: http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10020525-enable-roslyn-powered-data-asts-and-data-views
 [2]: /category/weekly-vote-reports/
 [3]: /2016/02/the-backwards-windows-platform-bridges-the-business-problem/