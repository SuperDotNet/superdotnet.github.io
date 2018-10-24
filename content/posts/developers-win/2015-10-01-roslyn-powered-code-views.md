---
title: Roslyn-Powered Code Views
author: Mike-EEE
type: post
date: 2015-10-01T21:49:19+00:00
excerpt: Introducing the idea of Code Views, a concept that allows developers to uniquely code their applications in a team/shared environment.
url: /2015/10/roslyn-powered-code-views/
mythemes-thumbnail-height:
  - 45
dsq_thread_id:
  - 4168679457
categories:
  - Developers-Win
  - General

---
### TL;DR: VOTE!

This post exists to build support around the idea of Roslyn-Powered Code Views. This is not intended to be a final solution, but a starting point for discussion, awareness, and a sign of demand. Show your support by voting for this idea here:

<div class="push-button-container"><div class="push-button">
</div><a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10020390-enable-roslyn-powered-code-views" target="_blank"><div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;"></div><img class="push-button-vote-text" src="/images/VoteNow.svg" /></a></div>

In this article, we explore the Visual Studio feature idea of what we are calling _Code Views,_ and is an idea that can now be made possible with the advent of <a href="https://github.com/dotnet/roslyn" target="_blank">Roslyn</a>.

### StyleCop

<div id="attachment_327" style="width: 500px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2015/09/ielz0.jpg"><img class="size-full wp-image-327" src="/wp-content/uploads/2015/09/ielz0.jpg" alt="The moment you realize that StyleCop is a File Format" width="490" height="266" srcset="/wp-content/uploads/2015/09/ielz0.jpg 490w, /wp-content/uploads/2015/09/ielz0-300x163.jpg 300w" sizes="(max-width: 490px) 100vw, 490px" /></a>
  
  <p class="wp-caption-text">
    The moment you realize&#8230;
  </p>
</div>

The nature of the problem we are attempting to solve revolves around a product known as <a href="https://stylecop.codeplex.com/" target="_blank">StyleCop</a>.  A code file is considered compliant when it satisfies all of StyleCop&#8217;s many (many!) arbitrary rules revolving around its definition of code style.  To dig a little further, the problem isn&#8217;t StyleCop&#8217;s fault _per se_, but rather the problem that it attempts to solve in that of a standardized style for code within projects.

### Eye of the Developer

StyleCop works wonderfully when you agree with all of its rules.  However, in practice you will find that is hardly the case.  The core problem with StyleCop&#8217;s approach is that it is attempting to place constrained limits on style, which is ultimately a very subjective quality.  Developers are incredibly creative individuals, and with that creativity comes strong opinions on a wide variety of matters, not the least of which is how to format the code that they create.

StyleCop&#8217;s view of style is just of one standard way of looking at code.  Furthermore &#8212; as you would expect for a subjective quality, as style is &#8212; many developers and organizations disagree with the (many) different rules of what StyleCop decrees and ultimately enforces.

_The result of using StyleCop is that individual developers lose the freedom to design their code in a manner that they wish to design it._

### Team Environments

This problem is not isolated to projects utilizing StyleCop.  Any developer who has worked in team environments know the pain of debating tabs vs. spaces or what line to place the opening brace.  These are all matter of style, and by agreeing to a &#8220;standard&#8221; style, ultimately one member&#8217;s definition of this style is what is enforced on all other members in the group &#8212; whether they like it or not.  Most developers simply go along for the sake of team unity.  Others will cause derision throughout a project&#8217;s lifetime by use of passive-aggressive commentary and thoughts behind the decided style.  Anyone who has been a part of such environment knows and understands the pain encountered here.

### Enter Code Views

Roslyn-powered Code Views would solve this problem.  With Code Views, Roslyn first loads code in as an <a href="https://en.wikipedia.org/wiki/Abstract_syntax_tree" target="_blank">AST</a> as it always does, but when it displays the code to the developer, it does so through a Code Formatting Profile that is configured to the developer&#8217;s preferences.  The developer then works in an AST that configured and presented precisely how they prefer it, maximizing their efficiency (and creativity).

<div id="attachment_311" style="width: 668px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2015/09/Open.png"><img class="wp-image-311 size-full" src="/wp-content/uploads/2015/09/Open.png" alt="Code Views: Opening a File" width="658" height="134" srcset="/wp-content/uploads/2015/09/Open.png 658w, /wp-content/uploads/2015/09/Open-300x61.png 300w" sizes="(max-width: 658px) 100vw, 658px" /></a>
  
  <p class="wp-caption-text">
    Code Views: Opening a File
  </p>
</div>

When the developer saves the file, the current Code View is then composed into a Roslyn AST, all known (configured) StyleCop rules are applied to it, and then saved back into the source code file, which should be 100% StyleCop-compliant.  The results of which could be checked-in to source control to the delight of all its members.

<div id="attachment_308" style="width: 751px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2015/09/Save.png"><img class="wp-image-308 size-full" title="Code Views: Saving a File" src="/wp-content/uploads/2015/09/Save.png" alt="Code Views: Saving a File" width="741" height="174" srcset="/wp-content/uploads/2015/09/Save.png 741w, /wp-content/uploads/2015/09/Save-300x70.png 300w" sizes="(max-width: 741px) 100vw, 741px" /></a>
  
  <p class="wp-caption-text">
    Code Views: Saving a File
  </p>
</div>

### Example Symbols and Format

To showcase some important concepts here.  Consider the following 100%-compliant StyleCop C# file:

<pre class="EnlighterJSRAW" data-enlighter-language="csharp">//-----------------------------------------------------------------------
// &lt;copyright file="Class1.cs" company="CompanyName"&gt;
//     Company copyright tag.
// &lt;/copyright&gt;
//-----------------------------------------------------------------------
namespace ClassLibrary2
{
    using System;
 
    /// &lt;summary&gt;
    /// Placeholder text for Class1
    /// &lt;/summary&gt;
    public class Class1
    {
        /// &lt;summary&gt;
        /// Placeholder documentation 
        /// &lt;/summary&gt;
        private int field;
 
        /// &lt;summary&gt;
        /// Placeholder text for method
        /// &lt;/summary&gt;
        /// &lt;param name="parameter"&gt;This is a description for parameter&lt;/param&gt;
        public void Method(int parameter)
        {
            var total = this.field = parameter;
            Console.WriteLine($"Hello World: {total}");
        }
    }
}</pre>

Now consider this same file as loaded and viewed after a theoretical Code Formatting Profile has been applied to it:

<pre class="EnlighterJSRAW" data-enlighter-language="csharp">using System;
 
namespace ClassLibrary2
{
    public class Class1
    {
        int _field;
 
        public void Method( int parameter )
        {
            var total = _field = parameter;
            Console.WriteLine( $"Hello World: {total}" );
        }
    }
}</pre>

Hopefully you can see all the adjustments made by the Code Formatting Profile.  It is configured to:

  1. Put using statements at the top of the file, rather than within the namespace.
  2. Start field names with underscores (you can imagine other profiles as even enabling Hungarian notation).
  3. Not use the &#8220;this.&#8221; qualifier.
  4. Not qualify private members with the &#8220;private&#8221; keyword.
  5. Put inner spacing around parenthesis (to let code &#8220;breathe&#8221;).
  6. Use tabs instead of spaces (unfortunately the highlighter used for the code above does not preserve this).
  7. Hide documentation.  Some developers feel English and XML get in the way of the only language that actually matters: C#.  Of course, enabling and viewing documentation is (or should be if implemented properly) a keystroke away.

### StyleCop as the Standard

By using Code Views, the developer saves their files to disk, and StyleCop rules are automatically applied to it to create a resulting code file.  The net result is that the file that is saved to disk is 100% StyleCop-compliant (or however compliant the team wants it to be).  This ensures that code is always in line with the style standard as currently offered by Microsoft. It also ensures a consistent, expected look and feel for any code that is stored on disk and (more importantly) in source control.

### Creative Freedom

By using Code Views, code files are stored on disk (or in the cloud) in a 100% industry-standard format, while developers are able to view their code exactly how they want and prefer to view it.  Through the use and power of Roslyn, this is now possible. Please take a second to vote for this feature request by clicking on our Vote Now button below. Or, if you have feedback around this idea, feel free to sound off in our awesome Disqus comment section below.  Thank you as always for your support!

### Show Your Support

If you like the idea of Roslyn-powered Code Views, please take the time and let Microsoft know by voting for this idea on UserVoice:

<div class="push-button-container"><div class="push-button">
</div><a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10020390-enable-roslyn-powered-code-views" target="_blank"><div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;"></div><img class="push-button-vote-text" src="/images/VoteNow.svg" /></a></div>