---
title: "July 2019 Update: Pivoting onto Blazor"
date: 2019-07-30T01:55:28-04:00
year: "2019"
draft: false
authors:
  - Mike-EEE
authorurl: "https://github.com/Mike-EEE"
tags:
  - Blazor
  - Art
  - Ethereum
  - Nethereum
categories:
  - Status
---

I suppose we can call this the July and August update since it is so late in July.

## Serializer

[Last I checked in](https://blog.superdotnet.run/2019/06/june-2019-update/), I believe I was bragging over the work and direction of working on the [serializer](https://github.com/SuperDotNet/Super.NET/issues/15).  While I have made some progress, my work has been sporadic and honestly missing some "heart."  I am not sure entirely for my lack of enthusiasm towards the goal.  However, I have identified the following:

1. Part of the friction here is that most of the work that I have done is already sufficiently addressed in the [ExtendedXmlSerializer](https://github.com/wojtpl2/ExtendedXmlSerializer).
2. While ExtendedXmlSerializer is probably the most recent personal development success I have had, it isn't exactly "wildly" popular -- with only 118 stars at the time of this writing.  Even at such a low level of interest, it still requires maintenance and time in fixing bugs and addressing issues.  Maybe not so much now as it ages and matures, but writing a whole new serializer from scratch will certainly have its own new issues and I am not sure that sounds exciting to produce and endure at this point.
3. The focus of a new serializer would be performance.  While this isn't the sole and premiere reason, there is a sense that while I attempt to develop it, I would be seeking to create the fastest-performing serializer of all.  In some since that is a valuable goal.  In another sense, however, it would be, to out-do a developer or team of developers in their own efforts.  I am not sure if this should be a guiding principle in development.

All that said, I might revisit the new serializer at some other point.  For now, I am going to focus on work that I find more appealing, if but for the exclusive concern of morale and momentum.

## Blazor Development

I am *so* very happy for [Blazor and its server-side application mode](https://docs.microsoft.com/en-us/aspnet/core/blazor/hosting-models?view=aspnetcore-3.0#server-side), which is what the original vision of this project encompassed.  Now, I do not have to develop it nor do I have to incur all the risk and bugs of doing so.

There are a few areas I would like to flesh out around this area, the first and primary of getting acquainted with Blazor and standing up my first application.  This is now what I will be focusing on accomplishing in lieu of serializer development.

## First Application

So, what is the first application?  Well, as I believe I have mentioned in other posts on this blog, one of my first dreams in life was to be a comic book artist.  Last year, I put together [an art project](https://ossem.com/) that revisited and unearthed that desire.

While I would not want to be *exactly* a comic book artist now, I first and foremost describe myself as an artist (or "creative").  For my first Blazor application, I am thinking of taking my art project and turning it into a store, whereby I can sell such art in a peer-to-peer manner via cryptocurrency ([Ethereum](https://www.ethereum.org/) via [Nethereum](https://github.com/Nethereum/), to be exact).

For reference, the first version of my art project -- as well as this blog that you are reading this on here -- is done with the amazing [Hugo](https://gohugo.io/).  I had considered progressing this art project with Hugo, but limitations prohibited some key functionality as Hugo is a static content generator and the functionality I envisioned required dynamic interaction and updating.

Now that Blazor is here, those limitations are lifted, and I am able to continue fleshing out this idea to see where it goes.

In doing such, I will be able to demonstrate capacity with Blazor, as well as provide a medium to continue developing my digital art (in penciling and perhaps even more).  And, since it is built as a store where I can sell items, I might make finally generate a revenue stream to boot.

At the very least, I will have made a site that demonstrates my capacity for software development and digital art, which might make a good item on my resume once I run out of money. 😆

There is lots to appreciate about this direction, so we will see where it goes.