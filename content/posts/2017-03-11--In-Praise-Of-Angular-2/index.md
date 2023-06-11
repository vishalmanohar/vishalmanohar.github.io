---
title: In Praise Of Angular 2
date: "2017-03-11T22:40:32.169Z"
template: "post"
draft: false
slug: "/posts/in-praise-of-angular"
category: "Software Development"
tags:
  - "swdev"
description: "Angular is a great improvement over AngularJS and can be a great choice for building single page apps, if you want a batteries included framework."
---

At my startup, our core application is built on AngularJS (1.x) and it was chosen for various reasons at that time. However, when there was a need to build additional applications last December, I was sure that I didn’t want to use Angular 1.x for those — mainly because it wasn’t satisfying nor fun to work on it especially with new and better alternatives like React and Angular 2 becoming mature.
I chose Angular 2 and I couldn’t be happier.

###Choosing Angular 2 vs React
For me, it eventually came down to choosing an end to end framework that provides all the functionalities required for a Single Page App versus choosing a library that builds views and leaving a lot of open decisions to make on view routing, an http service, architectural pattern, a build tool and others.
While the latter was tempting because it would have been fun to explore and choose different tools for each purpose, being in a lean start-up didn’t afford that option and we chose Angular 2 and a few months down the line, I couldn’t be happier with the choice.

###Feels a lot like AngularJS but 10x better
At a first glance, Angular 2 is bound to feel alien with the annotation heavy declarations and TypeScript syntax but play with it a little and if you have worked with Angular 1.x, you will soon relate to the same patterns like directives, HTML templates, dependency injection etc and ramp up pretty quickly. The egghead tutorial on Angular2 fundamentals really helped too.

##What makes it 10x better?

###Component driven design
With AngularJS, directives were the way to component-ize views so that they are modular for better organization, readability and reusability. However, the tendency in AngularJS was always to have fat Ng Controllers. With Angular 2, components (essentially directives) are the primary building blocks and there is no choice between an ng include controller or directives leading to a consistent pattern that is encouraged by the framework. In effect this led to much better modularity in the codebase.
State propagation is also much cleaner and explicit — where instead of using two-way binding of AngularJS, you use what is called as Event Emitters to signal state changes. Event Emitters and the Angular 2 http service use RxJS Observables which is a great fit!


###Angular CLI
If there was one thing that quickly pulled me into Angular 2 when I was just trying it, it was the Angular CLI which makes it super easy to get started building Angular apps. Angular CLI takes away all the chores you would have to do building a single page app — project skeleton set up, test framework setup (unit test and e2e), build set up, minification, environment configuration — so that you can focus on building features. The CLI uses webpack under the hood and if you want more control, you can always eject out of the CLI and use webpack directly — although I haven’t had to do this yet.


###TypeScript
Using typed Javascript is a joy on great IDE. Refactoring support, auto-complete features are much better with the type information but more importantly, using types enhances readability and the maintainability of the code. I have found myself diving into a codebase after a gap and found it at home primarily because the data structures were explicit. And TypeScript being a superset of JS, there isn’t a steep curve either and you can learn and discover things as you go.


###Performance

Angular 2 was designed to be mobile friendly and as such is faster than Angular 1.x and with AOT, it is a lot faster now with very little perceptible lag for initial rendering.


###Angular Universal
Server side rendering is still a thing if you to be friendly to Search Engines and Angular Universal framework makes it possible to set up pre-rendering pretty quickly. I haven’t used this so far but intend to soon.


In short, Angular 2 is a significant improvement on AngularJS and is a great option if you just want to run with an opinionated end to end framework.
