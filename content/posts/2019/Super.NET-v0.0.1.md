---
title: "Super.NET V0.0.1"
date: 2019-05-27T05:24:02-04:00
year: "2019"
draft: false
authors:
  - Mike-EEE
authorurl: "https://github.com/Mike-EEE"
tags:
  - dragonspark
  - dotnetcore3.0
  - xaml
  - wpf
  - cryptocurrency
categories:
  - Status
  - Releases
---

### Finally, Some Progress: v0.0.1

Today I am pleased to announce that [Super.NET v0.0.1 is completed](https://github.com/SuperDotNet/Super.NET/releases/tag/v0.0.1).

While that might sound exciting, it actually means nothing.  The v0.0.1 release is simply a foundational and framework release, intended to provide the core framework infrastructure to build components and supporting cast on top of it.

It stems from my previous work with its previous incarnation with the [DragonSpark Framework](https://github.com/DragonSpark/Framework), which was then taken in a pared down edition and utilized for [ExtendedXmlSerializer](https://github.com/wojtpl2/ExtendedXmlSerializer).

I have taken the results from those two projects and reconciled them in this v0.0.1 release.  This release is very basic and is not even offered as a nuget package -- I am waiting until v0.0.2 to offer such extravagances.  If you are interested in seeing it in its raw form until that time, however, [it is available here](https://github.com/SuperDotNet/Super.NET/releases/tag/v0.0.1).

### A Non-marketed Release

*Please note that I still have not marketed or promoted this project in any way*, except sharing it with close friends and family, as well as personally to those online that I feel would be interested (and sometimes they actually are 😆).

I started this project [last year around this time](https://superdotnet.run/), but was then confronted with about six months' worth of personal delays which I have [chronicled on this blog](https://blog.superdotnet.run/2018/12/attend-your-debts-real-and-imagined/).  Since April, however, it's been smooth sailing and I have been able to meet project goals and personal deadlines.

As far as promoting this project, it will not start until after the next phase of this project is complete: [the serializer](https://github.com/SuperDotNet/Super.NET/milestone/2).

### Next Up: v0.0.2

The next step is arguably the most important, and that is [the serializer](https://github.com/SuperDotNet/Super.NET/milestone/2).  To me, any project that is centered around presentation is only as strong as its serializer.  The best example of this is Windows Presentation Foundation, which has the *best* serialization model developed thus far with its Xaml system.

Lest we forget that a serializer is essentially the interface that allows a human to describe components that are instantiated, processed, and further rendered by a computer.

*In my view, this process is undervalued, overlooked, and for the most part entirely misunderstood in our current development culture and ecosystem.*

Thus, I will be attempting to build what is essentially the engine for this project for this next release, while also attempting to provide a worthy example of what I feel a serializer should be for the .NET ecosystem.

I should say that while performance is a goal, it is not the priority.  It *should* be faster than legacy seralizers, but *probably* not as fast as the new magic arising from .NET 3.0 core (although I will leverage what I can from there).  

*The primary goal and focus is to create an extensible serializer that re-establishes the spirit of the WPF Xaml serializer model, done in today's terms.*

### Remaining Work

You can see the established milestones that I have defined here.  I am essentially ballparking each release in 9-month increments, which is probably more than enough time but probably not.  And yes, you can connect the dots -- a nine-month release cadence makes these my babies.  😅

- [[**v0.0.2**](https://github.com/SuperDotNet/Super.NET/milestone/2)] 2020-04-07: The Serializer
- [[**v0.0.3**](https://github.com/SuperDotNet/Super.NET/milestone/3)] 2020-12-08: Client Presentation API
- [[**v0.0.4**](https://github.com/SuperDotNet/Super.NET/milestone/4)] 2021-12-21: Sample Hello Application 

(And yes, it is no coincidence that v0.0.4 is slated for the same date as [Silverlight's end-of-support](https://windowsreport.com/microsoft-silverlight/).)

For the hello world application, I have a neat idea for a cryptocurrency-based dApp (decentralized application).  Although, I am not entirely sure how decentralized it should be (as you will find if you study decentralized theory, there are many shades of this definition).  

(Part of the advantage/design of the long development times is to give me the opportunity to continue studying and analyzing the space for best approaches towards a viable solution.)

However, it should be simple, and at the very least show off all the core features and vision of what I am building here.

And at a worst case scenario, I will have built myself some resume material as I should be broke as a joke by then, ready for a new job. 😂

On that note, back to work.  Please take a second and [star me on GitHub](https://github.com/SuperDotNet/Super.NET). 🎉