---
title: "June 2019 Update"
date: 2019-06-06T23:20:29-04:00
year: "2019"
draft: false
authors:
  - Mike-EEE
authorurl: "https://github.com/Mike-EEE"
tags:
  - Ethereum
  - Nethereum
  - Blazor
  - WebAssembly
  - Ooui
  - PatternFly
  - Blazorise
  - PWA
categories:
  - Status
---

It's only been a few weeks since my last check-in.  Hey, I'm getting pretty good at this. 😆

### What's Up Now, Doc?

In my [last update](https://blog.superdotnet.run/2019/05/super.net-v0.0.1/), I left you with the impression that I was working on the Super.NET serializer.  This is still the case.  However, I have landed on a rather meaningful discovery that I wanted to share.

### Achieving the Ubiquitous (!)

You might be familiar with [Blazor](https://docs.microsoft.com/en-us/aspnet/core/blazor/get-started?view=aspnetcore-3.0&tabs=visual-studio).  I have been for a while, and have been discounting it as my impression was that it was exclusively [WebAssembly](https://webassembly.org/).

It turns out that this *not* the case.  Blazor is much like [Ooui](https://github.com/praeclarum/Ooui) -- or even [exactly](https://twitter.com/praeclarum/status/1136670167927103488) like it -- in that it has a "[server-side](https://docs.microsoft.com/en-us/aspnet/core/blazor/hosting-models?view=aspnetcore-3.0#server-side)" mode where the application's state is maintained by a WebSocket bridge between client and server.  This means the developer works exclusively in .NET and state is maintained seamlessly by the WebSocket bridge.  *And **this** means never having to explicitly work with JavaScript and working 100% within .NET.*

*For those keeping score at home, this is exactly what I had envisioned with this project.*

I cannot begin to describe how elated that makes me as I no longer have to "eat the world" with the amount of code I would have to write to make this a reality. 😇

### Mission Accomplished?

So, to me, **we're here**! 🎉  We're *finally* to a point where a viable solution can be made in .NET and used everywhere.

I am a firm believer that [progressive web applications](https://medium.com/@amberleyjohanna/seriously-though-what-is-a-progressive-web-app-56130600a093) are the future, and Blazor caters to this quite nicely.  With native store-hosted development, you are required to install ginormous SDKs and are confined to the policies and limits of the hosted store -- *for each platform*.

With HTML5/web-based development, there is none of that.  The only requirement is to install a browser, and with a modern device, that is already taken care of for you as the developer.

To me, there is only one way to develop in the modern marketplace, and that is HTML5.  The blocking issue up to this point is that there has not been a viable development paradigm for .NET, as they all required to work with JavaScript which is an expensive and unpleasant proposition.

Blazor *finally* fixes this.  However, there is a caveat.

### Eating the Ugly

The only misgiving that remains is that Blazor's syntax -- the Razor syntax and engine -- isn't Xaml.  It's a templating engine that intermixes HTML and .NET, the results of which are documents that look Frankenstein in nature, mixing views with code and looks *nothing* like Xaml.

However, all things considered, I am OK with this.  It is at least in a place where it is palatable.  The Razor engine is powerful, and there is a lot to be said about its [Razor Component model](https://docs.microsoft.com/en-us/aspnet/core/blazor/components?view=aspnetcore-3.0).  In fact, when you add in components from a framework like [Blazorise](https://blazorise.com/) or [PatternFly](https://github.com/WildGums/Blazorc.PatternFly), the markup looks more [Pascal-cased](https://www.quora.com/What-is-the-difference-between-Pascal-Case-and-Camel-Case) and Xaml-like.

One could even take this a step further and introduce more `ComponentBase`'s, and replace the `div` and `p` with `Container` and `Paragraph`.  At least, I am considering as a personal endeavor.

### What's Next?

These developments sort of put me in a bind, because now, the point of a serializer is -- at this point -- moot and non-obvious.  Recall that the serializer was meant to be able to describe POCOs that later get emitted as HTML.  This is no longer necessary as Blazor templating will take care of that problem space altogether.

The major consideration is that .NET Core 3.0 and Blazor will not be released until November.  That is still a lot of time to work out major issues and bugs -- bugs that one would have to be working with during that time.  I am inclined to continue work on the serializer during this time anyways as I would like something in my back pocket to know that I serialize any .NET object in case that I need to do so.

It also gives me time to start thinking about the first client application to build.

#### Client Application

Speaking of which, a solid shout of respect to [Juan Blanco](https://github.com/juanfranblanco) for his overwhelmingly impressive [Nethereum project](https://github.com/Nethereum/Nethereum).  He actually has a working Blazor application [that is available here](https://github.com/Nethereum/NethereumBlazor) and I have been exploring it.  [Ethereum](https://www.ethereum.org/) is one of the blockchain technologies that I have been researching, along with [EOS](https://github.com/eosio).  I would like to build an application (or two 😁) on these platforms.

It's great to see Mr. Blanco's work and efforts established and already taking hold.  Check it out and [star his repo](https://github.com/Nethereum/Nethereum/stargazers)!

Having Nethereum along with Blazor is a boon, as now all major the pieces are in place to develop a client application and really start creating again.

### Signing Off

Now that Blazor has arrived and a ubiquitous .NET solution is (*finally!*) upon us, I am not sure of my efforts here with Super.NET at the moment.  Perhaps I will make it a generalized framework around Blazor, perhaps I might close it altogether.  I still have not marketed or promoted this project and to be honest, I am sort of glad I haven't.

All that said, I am not sure when the next update will arrive.  I know it seems like I say that with every post, haha.  But, if I do have something interesting to say, I will be sure to post it here.  Maybe I will get into serialization and make a few posts around that.

Stay tuned. 🎉