---
title: Data ASTs and Data Views
author: Mike-EEE
type: post
date: 2015-10-01T21:57:28+00:00
excerpt: Introducing the concept of Data Views, enabling developers to work with data in the format that they prefer.
url: /2015/10/data-asts-and-data-views/
featured_image: /wp-content/uploads/2015/09/55ef453b4812941c66a30b48_Social-Profile-Thick-2561.png
mythemes-thumbnail-height:
  - 45
dsq_thread_id:
  - 4177937428
categories:
  - Developers-Win
  - General

---
### TL;DR: VOTE!

This post exists to build support around the idea of Roslyn-Powered Data Views. This is not intended to be a final solution, but a starting point for discussion, awareness, and a sign of demand. Show your support by voting for this idea here:

<div class="push-button-container"><div class="push-button">
</div><a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10020525-enable-roslyn-powered-data-asts-and-data-views" target="_blank"><div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;"></div><img class="push-button-vote-text" src="/images/VoteNow.svg" /></a></div>

### Data Views

In this article, we introduce a new idea that is possible now with the arrival of Roslyn: Data Views.  To be sure, Roslyn currently only supports C# and VB.NET as languages with which it can parse, load, and generate ASTs (abstract syntax trees). Data Views would require an extension to Roslyn to support what we&#8217;re calling Data ASTs to supplement its currently supported code-based ASTs. But, before we get into the details of Data ASTs and their subsequent Data Views, let&#8217;s first talk a little bit about the problem these concepts are meant to address.

### The Problem

The problem at hand is one that is becoming more and more common these days: JSON vs XML.  Developers are finicky about their preferred data formats as they are with their code, and it is becoming more and more common that one set of developers prefer XML while others prefer JSON. The fight doesn&#8217;t just stop at JSON vs. XML, either. It seems as if more and more data formats are coming to the table to &#8220;rescue&#8221; developers from all their perceived data format problems. This (ironically) serves to only make the problem worse by adding more options (and subsequent confusion and consequence) to the field. To give some context of breadth of this issue, here is a short list of possible data formats that are currently in use and available to the web and .NET development ecosystems:

  * <a href="https://en.wikipedia.org/wiki/XML" target="_blank">Xml</a>
  * <a href="https://en.wikipedia.org/wiki/Extensible_Application_Markup_Language" target="_blank">Xaml</a>
  * <a href="http://developers.squarespace.com/what-is-json/" target="_blank">Json</a>
  * <a href="http://json5.org/" target="_blank">Json5</a>
  * <a href="http://whatis.techtarget.com/fileformat/INI-Initialization-file-Generic" target="_blank">Ini</a>
  * <a href="https://en.wikipedia.org/wiki/YAML" target="_blank">YAML</a>
  * <a href="https://www.npmjs.com/package/tomljs" target="_blank">TOML</a>

&#8230; and much, much more! 😉

A team that prefers order over insanity will choose an official data format for their project.  Sometimes teams will get lucky and all members will agree on the type of data format to use for a project. When developers disagree on the preferred format, the heart of the problem we are exploring emerges. Ultimately, a developer will end up having to manage, maintain, and interact with a file format that they do not prefer. This may or may not lead to developer angst that can only move to hurt a team as its project progresses.

Much like the proposed solution to the problem of conflicting code styles, the preferred solution is not to fight and bicker about one &#8220;right&#8221; way over another. The preferred solution is to enable the developer to work in the format they prefer, while ultimately persisting the file data in the format that the team prefers.  This preferred solution is made possible through the use of Data ASTs and Data Views.

### Data AST

A Data Abstract Syntax Tree would exactly like a code-based abstract syntax tree, only in this case, the AST would be describing a data graph rather than a code graph. Once a Data AST is loaded into memory, it can be manipulated and used in the same ways a code AST can be manipulated and used from the Roslyn API.  Once a Data AST is loaded and available, it makes the Data View possible, and this is what is used by the developer so that they can work with their preferred format.

### Data View

The Data View is much like the Code View we discussed in the last article.  Here, the process starts with a data file (in any recognized/supported data format) that has been loaded from disk, parsed as a Data AST, and then run through a Data Formatting Profile that is defined by the user.  The ultimate result of this process is the Data View and it is what the developer uses to edit the data.

<div id="attachment_319" style="width: 672px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2015/09/OpenData2.png"><img class="wp-image-319 size-full" src="/wp-content/uploads/2015/09/OpenData2.png" alt="Data View: Opening a File" width="662" height="135" srcset="/wp-content/uploads/2015/09/OpenData2.png 662w, /wp-content/uploads/2015/09/OpenData2-300x61.png 300w" sizes="(max-width: 662px) 100vw, 662px" /></a>
  
  <p class="wp-caption-text">
    Data View: Opening a File
  </p>
</div>

Once the data has been edited, the developer can save the file, and the same process that happens with the Code Views is applied to the Data View to ensure a valid data file that is persisted to disk. On save, Visual Studio utilizes Roslyn to load and parse the data in the Data View to create a Data AST.  Once the Data AST is created, it is converted into the target and desired data format and formatted according to the preferences of the team or project.  This saves a file in a format that is desired by the team, and is ultimately what can be checked-in or used as an artifact for an external workflow.

<div id="attachment_321" style="width: 746px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2015/09/Untitled-Diagram-1.png"><img class="size-full wp-image-321" src="/wp-content/uploads/2015/09/Untitled-Diagram-1.png" alt="Data Views: Saving a File" width="736" height="177" srcset="/wp-content/uploads/2015/09/Untitled-Diagram-1.png 736w, /wp-content/uploads/2015/09/Untitled-Diagram-1-300x72.png 300w" sizes="(max-width: 736px) 100vw, 736px" /></a>
  
  <p class="wp-caption-text">
    Data Views: Saving a File
  </p>
</div>

### Formatting Freedom

Again, much like our desired goal with Code Views, the result here is to enable developers to have the freedom to work with the data formats that they prefer, rather than the formats that are decreed and dictated to them.  If you like this idea, please take a second and click on our cool Vote button below to visit the UserVoice vote and tell the Visual Studio team you would like to see this feature created. Additionally, if you have any feedback, please provide it in our awesome Disqus comments below. Thank you for your time, consideration, and support!

### Show Your Support

If you like the idea of Roslyn-Powered Data Views, please take the time and let Microsoft know by voting for this idea on UserVoice:

<div class="push-button-container"><div class="push-button">
</div><a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10020525-enable-roslyn-powered-data-asts-and-data-views" target="_blank"><div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;"></div><img class="push-button-vote-text" src="/images/VoteNow.svg" /></a></div>