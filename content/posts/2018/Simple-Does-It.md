---
title: "Simple Does It"
date: 2018-07-05T10:58:52-04:00
year: "2018"
authors:
  - Mike-EEE
authorurl: "https://github.com/Mike-EEE"
tags:
  - Mike-EEE
  - Hugo
categories:
  - Philosophy
  - Design
  - Psychology
---

This is an article on the topic of [philosophy in software, business, and life](/2018/07/philosophy).

As I mentioned in describing [software as a craft](/2018/07/software-as-a-craft/), I have been going through a very inspirational time with putting this project together.  In this section, I hope to explore a little bit about software design in general and some of the great appreciation that I have acquired by studying [Hugo](https://gohugo.io/), the very software used to produce and publish the content you are now reading.

## Hugo as an Example of Elegance

What is so inspiring about Hugo?  Well, I would say first and foremost, it's simplicity.  It also doesn't make assumptions, which you will see throughout its documentation.

The other aspect I appreciate is that it uses the file system as the data store.  That is, you are able to explore your website in a very accessible manner without having to configure and dive into the guts of a database.  In my view there has yet to be a good database tooling experience.  It has always been a lot of friction to access and manage your data there.  It also has been *completely different* from every other resource that you work with in a typical development scenario.  If you want to update data, you have to write a query.  Whereas with your code and every other artifact you work with, you simply save a file. 

This seems more consistent and congruent to me, hence the appeal.

Now, it's not all roses and candy here.  There are other challenges that the database is good at, such as doing mass edits or having a single row encapsulating the value of a frequently-used text string used throughout your application.  You are going to have to resort to error-prone find/replace methods here to adjust to those scenarios.

However, I think that's a healthy trade off.  In my view, anything that can limit the reach of a database, the better.  Again, I simply have not been a fan of it.  Consider that the website that you are now reading is the third website that I have created with Hugo.  Most of my time has been spent creating content.  I must have spent what feels like 3 full days learning Hugo and the rest in creating the content.

That to me is an enormous success in design.  It's worthy of praise and mention, and that is what this article is about.

It would seem that software these days has been taking a turn towards simplicity in general.  A "back to basics" approach, if you will.  This is something that I think is worth exploring, not only in form as presented in the products such as Hugo that we see today, but also from a more historical perspective.

## Over-architecture as a Defense Mechanism

While studying Hugo, it got me to think about what we have been putting up with as .NET developers, and why.  From my perspective I thought of a few aspects and thought I would share them.  This will serve as a bit of a retrospective in my own journey of having developed now for over twenty years.

> Always be asking yourself: who are you trying to impress, and why?

From my own experience, I can say that I have been very attracted to complex design.  Huge frameworks such as [Enterprise Library](https://docs.microsoft.com/en-us/previous-versions/msp-n-p/ff648951(v=pandp.10)) for instance, and of course, WPF and Silverlight.  I would spend hours and hours learning these frameworks.  I am going to use Enterprise Library as the outlining example here as pretty much every developer has had their hands and minds in WPF and Silverlight since that was assumed and necessary in our work.

Enterprise Library is a good example as I found that a lot of projects didn't use it, even though I thought it should.  Most thought it was simply too complicated, and, as it turns out, they were right.  This didn't stop me from exploring, it, however.  And in turn always recommending it to clients for solutions that I would be building for them.

The problem here is that once you develop a overly-complex system, you have to *support* that system.  You are also asking other developers to take the same path as you have and invest all their time into that system.  This has a cascading effect throughout an ecosystem, especially when that code originates from [MSFT](https://blog.superdotnet.run/2018/06/msft-vs-ms/).

The pitfall to be aware of here is that writing *a lot of code* can be a way of trying to *impress* others, or to make them think that you are smarter than you really are.  More code is not necessarily better.  I have been guilty of this for sure, having mimicked MSFT's style of creating large frameworks and probably with a lot of code that was not necessary (always a learning lesson and I am not saying I have exactly learned it with finality just yet).

This is not to say that software shouldn't be complex.  I can guarantee you the code I will be writing will certainly be.  But the point here is to be *mindful* of this condition.

Always be asking: who am I trying to impress, and why?

Personal self discovery and reflection is as an important tool in every developer's tool kit as any software library.  Be sure to constantly assess your own motivations and what drives you to make the decisions you do.  I know it's something that I constantly monitor in my own world and I do not have very good answers for a lot of them.  But, I would say *mindfulness* of this is a good first step.

#### Other Lessons Learned

I think this is a good spot to mention other lessons learned throughout my development history in a blog post that you can [read here](https://blog.superdotnet.run/2018/06/hello-world-welcome-to-super.net-blog-dawg/#lessons-learned).

## Incorporating Greatness

The great part about having other, foreign technology projects is that you can utilize them as [inspiration to incorporate into your own works](https://en.wikipedia.org/wiki/Ren%C3%A9_Girard#Mimetic_desire).  You can be assured that I will be keeping Hugo in mind as I move forward here with Super.NET and other software endeavors.