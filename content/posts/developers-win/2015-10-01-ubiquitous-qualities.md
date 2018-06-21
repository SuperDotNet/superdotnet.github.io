---
title: Ubiquitous Qualities
author: Mike-EEE
type: post
date: 2015-10-01T19:59:43+00:00
excerpt: 'The Bridge to .NET Ubiquity: Ubiquitous Qualities. In this article, we outline the desired and expected qualities for a ubiquitous .NET client application development model.'
url: /2015/10/ubiquitous-qualities/
featured_image: /wp-content/uploads/2015/09/Transpile.png
mythemes-thumbnail-height:
  - 45
dsq_thread_id:
  - 4184221916
categories:
  - Developers-Win
  - General
series:
  - The Bridge to .NET Ubiquity

---
<div class="seriesmeta">
  This entry is part 2 of 6 in the series <a href="/series/bridge-to-dotnet-ubiquity/" class="series-6" title="The Bridge to .NET Ubiquity">The Bridge to .NET Ubiquity</a>
</div>

### TL;DR: VOTE!

This series exists to build support around the idea of a ubiquitous .NET client application development model.  This is not intended to be a final solution, but a starting point for discussion, awareness, and a sign of demand. Show your support by voting for this idea here:

<div class="push-button-container"><div class="push-button">
</div><a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10027638-create-a-ubiquitous-net-client-application-develo" target="_blank"><div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;"></div><img class="push-button-vote-text" src="http://uploads.webflow.com/55e079ccd960e71226582014/55d09ab72123fb7e3e46b1cd_Vote%20Now!%20Text.svg" /></a></div>

### Desired and Expected Qualities

In this article, [we][1] outline the desired and expected qualities for a ubiquitous .NET client application model. The purpose of this article is to not only provide a vocabulary and context of definitions used later on in subsequent articles, but to also provide a fuller meaning of precisely what we mean when we say a &#8220;ubiquitous .NET client application model.&#8221; Ubiquity and ubiquitous implies an essence and expectation of _everywhere_, and while that is certainly the primary expected and desired quality of what we would like to achieve, there are other technical requirements at play that should also exist in any designed (and desired) ubiquitous .NET client application model.

Below, you will find the list of these qualities in full. Please note that we consider _qualities_ as _requirements_ and will use these terms interchangeably. In the next post, we will be using these qualities to demonstrate that no existing client application model possesses the desired requirements to be considered a truly _ubiquitous_ .NET client application model.

### <img class="requirement-icon alignnone wp-image-277" title="Native Cross-Platform Capable" src="/wp-content/uploads/2015/09/Cross-Platform-300x300.png" alt="Native Cross-Platform Capable" width="60" height="60" srcset="/wp-content/uploads/2015/09/Cross-Platform-300x300.png 300w, /wp-content/uploads/2015/09/Cross-Platform-150x150.png 150w, /wp-content/uploads/2015/09/Cross-Platform.png 400w" sizes="(max-width: 60px) 100vw, 60px" /> Native Cross-Platform Capable

Let&#8217;s start with the easy one first. It seems as if this is a prevalent and expected requirement and capability these days. A ubiquitous client application should expect to run on workstations and desktops, as well as mobile devices and the various platforms that support each of these form factors. The major players and expectations are:

  * Windows
  * iOS / Macintosh
  * Droid / *nix (Unix/Linux)

Microsoft has done a great job opening up to the different platforms outside of Windows. However, this is not the case for any of their current client application models, as all of them (with the exception of the ill-fated Silverlight) remain strictly a Windows-only affair. A ubiquitous client application model is satisfied by running on all of the major platforms outlined above.  The expectation for a ubiquitous .NET client application development model is that it will be built into artifacts that will run on the target platform in a native way.

### <img class="requirement-icon alignnone wp-image-279" title="HTML5-Compliant" src="/wp-content/uploads/2015/09/HTML5-300x300.png" alt="HTML5-Compliant" width="60" height="60" srcset="/wp-content/uploads/2015/09/HTML5-300x300.png 300w, /wp-content/uploads/2015/09/HTML5-150x150.png 150w, /wp-content/uploads/2015/09/HTML5.png 400w" sizes="(max-width: 60px) 100vw, 60px" /> HTML5-Compliant

In addition to native cross-platform capable, a ubiquitous client application must also operate and work in an HTML5-compliant runtime environment, such as a web browser. This is where all existing Microsoft-created client application models fail, and where much of the marketplace confusion and developer angst resides. Microsoft does not offer a client-side web client application model. The only offering they provide is a client application model that operates on the server-side via ASP.NET. A ubiquitous client application model would execute within an HTML5-compliant runtime context just as it does with a native cross-platform runtime context, and operate the exact same way. The big hurdle to this problem is that .NET is compiled into IL/bytecode, and this is inherently incompatible with web architecture (or JavaScript). However, as we will [demonstrate in a later article in this series][2], Microsoft can work towards solving this barrier and make this a commonplace reality for .NET through the use of transpilation.

### <img class="requirement-icon alignnone wp-image-280" title="Consistent User Experience" src="/wp-content/uploads/2015/09/UX-150x150.png" alt="Consistent User Experience" width="60" height="60" srcset="/wp-content/uploads/2015/09/UX-150x150.png 150w, /wp-content/uploads/2015/09/UX-300x300.png 300w, /wp-content/uploads/2015/09/UX.png 400w" sizes="(max-width: 60px) 100vw, 60px" /> Consistent User Experience

When we speak of a ubiquitous client application model, the expectation is that its user experience is the same no matter what device or platform from which it is viewed. This is much in the same way an HTML5 web page looks and feels the exact same way no matter the browser or OS used to load and view it. In a ubiquitous .NET application, the expectation is that this quality is preserved, and all clients everywhere &#8212; no matter the platform or device &#8212; provide the exact same user experience to the user. In addition to consistency, this offers strength and value to the model at large, as it asserts its own unique perspective on user interaction and this reinforces its brand in the marketplace (much like HTML5).

### <img class="requirement-icon alignnone wp-image-281" title="Cross-Boundary Accessibility" src="/wp-content/uploads/2015/09/Cross-Boundary-150x150.png" alt="Cross-Boundary Accessibility" width="60" height="60" srcset="/wp-content/uploads/2015/09/Cross-Boundary-150x150.png 150w, /wp-content/uploads/2015/09/Cross-Boundary-300x300.png 300w, /wp-content/uploads/2015/09/Cross-Boundary.png 400w" sizes="(max-width: 60px) 100vw, 60px" /> Cross-Boundary Accessibility

When we conceptually explore a .NET ubiquitous client model, we find that it is one model found within a bigger solution, which in turn is comprised of other projects based on other application models. In a typical .NET solution, you have an application running on the service/cloud tier (the &#8220;service boundary&#8221;) and then the client application running in its tier (the &#8220;client boundary&#8221;). The beauty of .NET is that developers can create artifacts &#8212; in particular _assemblies_ &#8212; that can be shared in both the server and the client boundary. This is usually done via the implementation of a _shared or common assembly_. This is a very powerful quality, as it keeps encapsulation intact, and honors the principle of <a href="https://en.wikipedia.org/wiki/Don%27t_repeat_yourself" target="_blank">DRY</a>. A ubiquitous client application model will allow for this. Currently, this quality is prohibitive (and as we will see, organizationally expensive) in HTML5-hosted scenarios, as artifacts are created using JavaScript, which is completely incompatible with .NET or any of its compiled assemblies.

### <img class="requirement-icon alignnone wp-image-282" title="Xaml-Powered" src="/wp-content/uploads/2015/09/XAML-150x150.png" alt="Xaml-Powered" width="60" height="60" srcset="/wp-content/uploads/2015/09/XAML-150x150.png 150w, /wp-content/uploads/2015/09/XAML-300x300.png 300w, /wp-content/uploads/2015/09/XAML.png 400w" sizes="(max-width: 60px) 100vw, 60px" /> Xaml-Powered

Xaml is probably one of Microsoft&#8217;s greatest inventions and it really does not seem to get the acclaim it deserves. When we speak of Xaml, **we speak of the Xaml model that is found in Windows Presentation Foundation and Silverlight 5 as the model to compare all other subsequent Xaml models**. Both of these client application models feature the best and most powerful Xaml capabilities in comparison to any of the other client application models out there today. It is also important to note that **<a href="https://imgflip.com/i/h6ho2" target="_blank">Xaml is not just a mechanism for defining user interface elements</a>**, but a powerful and expressive mechanism to describe **_any_** .NET object in very elegant and creative ways. It is a serialization mechanism with concepts that are not found in any other serialization framework, and this is why it is so powerful and fun to work with as a developer. In addition to serialization, Xaml development benefits from strong tooling and designer support found in Visual Studio. Any ubiquitous .NET client application model should be powered by these mature and tested capabilities and features that Xaml affords.

### <img class="requirement-icon alignnone wp-image-283" title="Object Serialization Congruence" src="/wp-content/uploads/2015/09/Serialization-150x150.png" alt="Object Serialization Congruence" width="60" height="60" srcset="/wp-content/uploads/2015/09/Serialization-150x150.png 150w, /wp-content/uploads/2015/09/Serialization-300x300.png 300w, /wp-content/uploads/2015/09/Serialization.png 400w" sizes="(max-width: 60px) 100vw, 60px" /> Object Serialization Congruence

Serialized congruence is a quality that describes the intent of an object that is described and serialized via a markup language. When we say that an object has serialized congruence, we mean that the object that is created in memory is the same as the object that is defined and described in the serialized file. Another way of looking at this quality is that the external matches the internal. For example, consider the following markup:

<pre class="EnlighterJSRAW" data-enlighter-language="html">&lt;Apple&gt;&lt;/Apple&gt;</pre>

When this object has been deserialized and viewed in memory, we should expect an object of type Apple that was created and stored there, not an Orange or Banana. That is, there is a 1:1 correlation between what was defined and described in the serialized file versus what we ultimately find in memory. Because of this, the class definition of the object becomes its schema. This is very helpful for both tooling and design (not to mention the developer). Additionally, this also optimizes resources as now a developer (and tools) only need to know about two artifacts: the serialized data file and the class file as its schema.

Now consider another example that might create an Apple in memory after it has been serialized:

<pre class="EnlighterJSRAW" data-enlighter-language="html">&lt;object add="Fruit" type="Apple" /&gt;</pre>

In this case, special logic exists somewhere that ultimately does a lookup on a string to determine the action to perform (activate an object). A subsequent attribute lookup on the &#8220;type&#8221; property is also used to resolve the type used for activation. The result is ultimately the same (an Apple is created) as the previous example, but in this example, the data provided here does not accurately reflect the nature of this ultimate result. This is not a 1:1 correlation of the describing data to the desired initialized object and is therefore not congruent.

Additionally, a separate file must now be created and stored that defines the schema of this data file, and kept in sync with the object that it is defining. This produces three artifacts: the serialized data file, the class it is defining, and the schema used to define the data file. This is costly from a resource perspective (more bytes and files on disk) and also from a developer perspective, as developers now have to locate, link, and keep track of additional unnecessary files when managing data definitions of objects when utilizing this design.

Now, let&#8217;s move from fruits to a more practical example using a client-side component. In particular, we will use an object that can be used to display elements within it:

<pre class="EnlighterJSRAW" data-enlighter-language="xml">&lt;DockPanel&gt;&lt;/DockPanel&gt;</pre>

This makes sense and seems congruent. We are defining a DockPanel object and when the serialization mechanism processes the data (xml) and loads the object in memory, we should expect to see a DockPanel.

Now, let&#8217;s see another example of how this object might be defined in another client application model, specifically HTML5:

<pre class="EnlighterJSRAW" data-enlighter-language="html">&lt;div class="dock"&gt;&lt;/div&gt;</pre>

By now the example and premise should be clear. We are intending to describe a DockPanel, but are creating an object in memory that is not this object, but more than likely behaves like a DockPanel. This is not congruence, as what is defined in data (xml &#8212; or the _external_) is not ultimately what is created and loaded into memory (the _internal_). This is again costly on two different fronts: in the tooling built accounting for this design, and with the developer having to comprehend and accurately understand its conceptual nature.

At this point, it should be obvious that Xaml-based application development caters to this requirement perfectly, as objects are accurately defined and serialized with absolute congruence.

### <img class="requirement-icon alignnone wp-image-284" title="Holistic Development Consistency" src="/wp-content/uploads/2015/09/Holistic-Dev-150x150.png" alt="Holistic Development Consistency" width="60" height="60" srcset="/wp-content/uploads/2015/09/Holistic-Dev-150x150.png 150w, /wp-content/uploads/2015/09/Holistic-Dev-300x300.png 300w, /wp-content/uploads/2015/09/Holistic-Dev.png 400w" sizes="(max-width: 60px) 100vw, 60px" /> Holistic Development Consistency

Finally, we have the issue of holistic development consistency. This goes along with the requirement of cross-boundary artifacts and assemblies. This occurs when the same naming and development guidelines are applied equally to all projects within a solution uniformly. That is, objects that are defined and used in the server tier use the same development guidelines that are used in the client tier. Guidelines are rules that apply to concepts such as naming, capitalization, member definitions, and type definitions. .NET has a very comprehensive set of guidelines and <a href="https://msdn.microsoft.com/en-us/library/ms229042(v=vs.110).aspx" target="_blank">they can be found here</a>.

The guidelines and rules for the development concepts we are discussing are completely different in certain application models than others. In particular, you will find very different guidelines used in JavaScript and even TypeScript. Most &#8212; if not all &#8212; of the prescribed design guidelines for these languages are at odds with the .NET design guidelines. Therefore, adding an HTML5 client application to a .NET solution offers a completely different set of rules and protocols that developers must follow when compared to all of the other projects within their solution. This leads to context-switching which can affect quality and lead to mistakes, as a developer must always consider the mode they are in before developing their solution. Time taken to consider context is time taken from getting to the problem at hand.

### Applied Requirements

In the next post of this series, we will search for the qualities defined above in all the known major and upcoming .NET client application models. Through this exercise, we hope this will help demonstrate what we are after when we envision and articulate a ubiquitous .NET client application model, while also underscoring that no one model can truly be considered ubiquitous in the current market climate.

### Show Your Support

If you like the idea of a ubiquitous .NET client application development model, please take the time and let Microsoft know by voting for this idea on UserVoice:

<div class="push-button-container"><div class="push-button">
</div><a class="w-inline-block top-lighting" href="http://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/10027638-create-a-ubiquitous-net-client-application-develo" target="_blank"><div class="glass-insert" data-ix="blink" style="transition: opacity 500ms ease-in-out; opacity: 0;"></div><img class="push-button-vote-text" src="http://uploads.webflow.com/55e079ccd960e71226582014/55d09ab72123fb7e3e46b1cd_Vote%20Now!%20Text.svg" /></a></div>

 [1]: /2015/10/introduction/#who-are-you-who-is-the-8220we8221
 [2]: /2015/10/the-ubiquitous-bridge/