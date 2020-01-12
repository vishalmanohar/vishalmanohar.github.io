---
title: Architecture In The Age Of Agile
date: "2015-05-12T22:40:32.169Z"
layout: post
draft: false
path: "/posts/agile-software-design"
category: "Software Development"
tags:
  - "swdev"
description: "Does agile software development mean you don't do any upfront architecture?"
---

One of the things that I try to keep in mind while working on code is [this quote by Martin Fowler](http://martinfowler.com/bliki/PairProgrammingMisconceptions.html):

>If I'm writing boring repetitive code it's usually a sign that I've missed an important abstraction, one that will drastically reduce the amount of rote code to write

In Agile, you work in small iterations (week or two weeks at the most) and developers tend to work on work on different parts of the application and diverse features almost every day (pair rotation). So, unless there is a constant reflection of what you are doing, it is easy to miss the forest for the trees, or in our case the important abstractions that can solve a whole class of problems efficiently.

A lot of the code level abstractions like say, validation framework or error handling etc. would be naturally implemented while working on code but it can be difficult to identify high level abstractions when you are knee deep into a specific problem and it is much more efficient to identify them ahead of time.

For instance, for an application that needs to build adapters to various gateways like MQ, FTP, filesystem, email, etc. can we consider integration frameworks like Apache Camel or Spring?

Or, if you are building a CRUD interface, is it possible to build a generic solution using a meta-model approach like [this](https://www.playframework.com/documentation/1.2.3/crud)?

So, while Agile development eschews big up-front design it is still important to have a high level design in mind with the difference being that in Agile, the plans are not set in stone and can evolve based on changing scope and new learnings.  This [article](http://www.infoq.com/news/2010/05/agile-architecture-partnership) delves into the inherent tension between agility and upfront planning and design.