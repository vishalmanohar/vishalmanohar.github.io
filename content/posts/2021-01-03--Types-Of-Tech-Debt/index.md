---
title: Types of Technical Debt
date: "2021-01-03T18:40:32.169Z"
template: "post"
draft: false
slug: "/posts/types-of-technical-debt"
category: "Software Development"
tags:
  - "swdev"
description: "Understanding the taxonomy of technical debt can help anticipate and plan before last due date."
---

Technical Debt is a phrase that is most often used to refer to shortcomings in the software from a technical perspective.

The metaphor is attributed to Ward Cunningham, [who explained it as](http://wiki.c2.com/?WardExplainsDebtMetaphor):

> "The explanation I gave to my boss, and this was financial software, was a financial analogy I called "the debt metaphor". And that said that if we failed to make our program align with what we then understood to be the proper way to think about our financial objects, then we were gonna continually stumble over that disagreement and that would slow us down which was like paying interest on a loan."

While technical debt is most often used to refer to the design and code quality issues, it also has a broader applicability and being aware of the different types of debt can help plan and prioritize.


## Types of Technical Debt

### Quality of Code Debt

Most of the usage of the term technical debt refers to issues with code quality.
Below are some of the things that drags down quality of code:

#### Examples:
* **Code Smells**

  These are the "Code Smells" listed exhaustively in the [Refactoring](https://martinfowler.com/books/refactoring.html) book. Smelly code is not just an eye sore for anyone who reads it but is akin to a high amp resistor to enhance features on top of, besides being a source of defects and an anchor for developer morale.


* **Duplication of business logic**

  Most often done for a "quick and dirty" fix but also can be caused by lack of context with the developer.

  Business logic duplication often creates a whack-a-mole pattern of defects where each fix introduces an inconsitency in behaviour from its duplicates.

  Not all duplication incurs the same cost. E.g. Duplicating business logic like tax calculation in an invoicing module can be very costly since it can be source of bugs, whereas duplication of a small utility method although imperfect is not a big deal.

* **Hardcoding instead of driving by config**

  For e.g. using a custom logic against a customer identity to meet their immediate requirements.

  Often used for quick fixes or implemented for proof of concept but if not attended to, can languish and affect maintainability as the customer base grows.

* **Lack Of Tests**

  Test coverage is what gives confidence to change code and lack of sufficient coverage, atleast in the important workflows of the code is a huge debt.


* **Hard to Read**

  How easy is it for a new developer to understand a piece of code and relate it to business understanding? Does the code convey the intent properly?

  Is complex domain logic encapsulated using Domain Driven Design?

  Is the code organized in a structured manner around modules?

  How much of tribal knowledge is required for a new team member to make a low complexity change on their first week of work?


* **Lack of Observability**

  Are you able to observe what the system is doing in a production environment?

  Lack of logging in the code, lack of auditing user actions can severely impede maintainability and slow down resolution of customer issues.


#### Improving Code Quality
Code quality related issues become apparent once an application is in production and being enhanced. This can be visible in terms of defects or customer support tickets or unusally long times to make small changes.

Code quality issues can be budgeted whenever there is a change in the related area either to fix a defect or to enhance a business logic. For e.g. in a story or a ticket to enhance a feature, the team can also highlight the issues with the code that needs to be addressed.

Observability issues must be fixed as and when they are detected.

Automated code quality checks like PMD in java or Rubocop in Rails or JSLint in Javascript can help surface issues during development and can be a developer aid apart from code reviews.
However, quality of code is a function of the level of the craftsmanship on the team.

Besides pairing, doing refactoring workshops, [Refactoring](https://martinfowler.com/books/refactoring.html) book reading, DHH's set of videos on ["Writing software well"](https://www.youtube.com/watch?v=wXaC0YvDgIo&list=PL9wALaIpe0Py6E_oHCgTrD6FvFETwJLlx) have helped me to impress the importance of code quality and drive changes especially for new developers and teams that have been very tactical while coding.

### Abstraction Debt

The primarily leverage in software or a machine versus doing something manually is the ability to build abstractions so that the same thing can be used as many times in different contexts.

Consider a hardware fastenter like a nut and bolt. This primitive can be used to join parts together and is a fundamental building block in artifacts. This can be used to build tools which is then used to build even complex tools.

Likewise, software is composed using multiple primitives, which leads to a complex building block on top of which more complex things can be built.

>Well written software recognizes commonality of requirements and abstracts behaviour and concepts to provide the right primitives and abstractions on which more complex behaviours can be built.
Poorly written software often is a big ball of mud with rote code used to do the same things in different places and reveals itself when even small changes require a lot of effort.

Example - not using a layered design and making things reusable. Consider a shopping cart application. An order can be created from multiple sources - cart, special offer, subscription, external API etc. Well structured code will have a single internal API to create an order from different sources and not have multiple APIs for the same.

In a consulting engagement, working with an enterprise SaaS application, the reporting module did not have any abstraction for basic things like server-side pagination and filtering or role based filters. Each new report would get hand coded in its own way and over time the report count grew to over a 100. In the early stages of that enterprise product, there was not much data and this was passable. But as the data began to grow, performance issues due to lack of server side pagination revealed itself and these reports had to be re-written from the ground up.

Modern application frameworks like Spring Boot, Django, Rails already take care of providing web app primitives for HTTP request routing, database access, file storage, emails etc. But any non-trivial application will need custom abstractions to create leverage in software.

**Deferred abstractions**

However, an abstraction can be deferred until there is better clarity on requirements and use cases or until the [cost of delay](https://en.wikipedia.org/wiki/Cost_of_delay) is not viable.

Let's say in an enterprise product, each customer has complex data processing rules.  Not having an abstraction like a DSL or configurability in the rules is a debt because ability to express these rules easily is a much needed abstraction here. However, if the complexities and future needs can't be anticipated at the early stage with the first few customers, it might make sense to implement them using custom code for each customer without building a custom DSL or using a rule engine.
Here you are trying to avoid the cost of the wrong abstraction which can be much higher than the benefit.

A feature debt can also be a cause of the missing abstraction. Consider an example where each customer for enterprise product expects a custom invoice template. An Invoice Template Builder UI is ideal but depending on the product and the number of customers, this can be deferred and instead built as custom template per customer if there are more important features to focus on until it becomes a pain point. Here, the cost of delay is an important metric to measure if this should be done.

Missing abstractions are usually due to lack of tech leadership in the team.

#### Preventing Abstraction Debt

* Abstractions provide the primary leverage in software development. Developers must constantly evaluate when something needs to be abstracted at the time of development.

* Be wary of the cost of building the wrong abstraction. The cost to dismantle it and replace will be much more expensive than deferring it and when there is better context.

* If a shortcut is used intentionally, call it out with the rest of your team. Use comments in the code to let other developers know about the context and how you think this might need to change.

* As the related feature evolves, evaluate whether it is time to put in a proper abstraction.

* [Cost of delay](https://en.wikipedia.org/wiki/Cost_of_delay) is a great measure to priotize work.

* Teams must have technical leaders who are able to think at a system level and consider these tradeoffs.


### Dependency Upgrade Debt

Code doesn't exist in isolation. Any non-trivial software application will have many many third party libraries and packages they depend on to build the software.

This is everything from the language version, to application framework version and other libraries used to accomplish specific tasks. And, each of them are also evolving over time just like your software.

This tends to be one of the most overlooked aspect of tech debt.
But the cost can be crippling especially for an application built on a dynamic language like Ruby and Python AND with low test coverage - where it is much harder to upgrade the language version and the application framework. Upgrades like Python 2 to 3 where there are a lot of breaking features is a nightmare.

In the Java world also, the 6 month release cadence has meant faster rollout of new features and shorter end of life cycles for support.

> Dependency upgrade debt is the cost you have to pay for not upgrading your dependency version periodically.


**Cost of dependency upgrade debt**

* Much bigger risk and effort to upgrade when the version distance is high.

* Online community support for a constantly evolving package version dwindles over time. Consider React Native. A lot of issues on their Github and Stackoverflow are so dependent on the version of the framework that if you have to overcome an issue that you are facing, it means you have to upgrade to a more recent version to even report the issue and get help.

* Older version API documentation might be discared. And with that you might even lose the documentation required to migrate from your current version to the next version incrementally.

* Miss out on bug fixes, new features, performance improvements, security vulnerability fixes.

* Risk of forced upgrade at the worst possible time. Consider, you run into a major performance issue that is getting a lot of customer tickets and you trace this to a dependency that hasn't been updated for many years. You discover that the issue has been on a new major version of the software.

* Inability to upgrade one package for a feature because it needs a higher version of another package. e.g. a lot of Django packages are compatible with the specific version of Django and you can't upgrade a package without upgrading Django itself.

#### Tackling Dependency Upgrade Debt

* Review dependency upgrades periodically - atleast once in a quarter and create action items.
* Use tools like [dependabot](https://dependabot.com/) to automate dependency upgrades.
* Keep the team aware of new releases in core packages by subscribing to RSS feeds in your Slack channel.

### Infrastructure Debt

Just like software dependency upgrade debt, your infra also needs constant upkeep.

Consider, Postgres database or elastic search service or a message queue. Each of these infrastructure pieces are also evolving constantly - which is good in terms of features and performance but it also means they need to be on your radar for upgrades.

Cloud Services are also constantly evolving with a slew of new features, capabilities and products being announced every year - whether it AWS, Azure or Google Cloud.

Each upgrade is an opportunity to leverage better features, performance or price that can improve your product.

**Cost of insfrastructure debt**
* Same as dependency debts
* Even lesser optionality on managed cloud services - for e.g. RDS on AWS stops support for older end of life versions of Postgres/RDS.

#### Tackling Infrastructure Debt
* Similar to dependency upgrade debt, infrastructure upgrades must be reviewed periodically within the team.
* Using containers to set up dependencies like DB, ElasticSearch etc locally and on CI can provide a lot of leverage to upgrade versions and go back and forth.
* Identify and groom expertise in the team around key infrastructure. For e.g. if your product uses MongoDB, Kubernetes, ElasticSearch, each of these should have members who are proficient in them.
* Use a Skill Matrix in the team to identify expertise gaps and review periodically to make sure that the gaps are closing.


### Closing Thoughts

Technical debt comes in many forms. Recognizing each and planning for it helps in managing it proactively.

Technical debt is a function of the quality of people in the team.
Are they passionate about their craft?
Do they have a good work ethic?
Are they curious to learn new things?
Are they able to communicate to the leadership about technical debt and influence decisions?

Finally, there is no substitute for experience and expertise in the team.
