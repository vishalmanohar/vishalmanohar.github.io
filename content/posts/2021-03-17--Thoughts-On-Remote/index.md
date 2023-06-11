---
title: Thoughts On Remote
date: "2021-03-01T18:40:32.169Z"
template: "post"
draft: false
slug: "/posts/thoughts-on-remote"
category: "Software Development"
tags:
  - "swdev"
description: "Remote work has tradeoffs and must be understood before applying it voluntarily"
---
(Incomplete draft)

## On Remote

Over the last 16 years in tech, I have had the opportunity to work remotely on several occassions, notwithstanding the Covid imposed remote work.

IT services companies notoriously don't encouraged work from home especially on time based billing projects, and it used to be on discretion. Product companies on the other hand, were always more relaxed on remote because outcome matters more than output and there are no timesheets to fill anyways.

In the last 1 year Covid imposed remote work wherever possible and software development particularly is well suited because you just need a laptop and internet connection to start working.

In any case Covid has changed perspectives on remote work forever - from outright skeptics who had to accept that it was possible to productive remotely to the pro-WFH rebel who now craves to go to the office :)

### What remote work enabled

* Save commute times (or reduce if working from nearby coworking space)
* More time for family and kids and better satisfaction in that sphere
* Lesser interruptions if you are able to block out Slack and other notifications and therefore larger chunks of time to focus on tasks
* Reduce energy depletion for introverts

### What an office enables but is challenging in remote

* Meetings - just harder to run with a lot of people.
* Face to face interactions that build trust and team work
* Huddles to brainstorm on an idea or tech design
* Mentoring new developers
* Physical isolation that allows one to keep away from distractions and other errands when working from home.
* Team building through water cooler conversations and group activities
* Energy refueling for extroverts
* Gauge well being of your team and employees and help them if required
* Shared understanding

### Other remote challenges

* Zoom fatigue
* Slack overload

### Compensating for gaps in remote

* Meeting memos

  Amazon's [unique meeting style](https://medium.com/@Elabor8/amazons-shift-from-presentation-culture-to-memo-culture-and-what-you-can-learn-from-it-a44f6db2c864) has been getting a lot of attention. Some of the immediate takeaways like having a clear agenda, documenting all the required context and references for the meeting can go a long way to make meetings effective and efficient.

* Emphasise Documentation

  A writing culture for everything from product requirements to design decisions (e.g. [ADR](https://adr.github.io/)) to process and HOWTOs help a lot in preserving context that would have been tribal knowledge in the team.

* Use tools like Quip / Notion that promote documentation
  Slack is great for real time context sharing but a poor medium for a knowledge base. Tools like Quip, Notion etc. which faciliate conversations around documents, go a long way to not only enable documentation but also preserve context. This automatically promotes documentation around a context.

  Google Docs with its comments feature is good too but its doesn't do a great job with comments. For e.g. the interactions on top of a comment are limited and others cannot upvote a comment or react to it. The author can resolve a comment and it is then lost - so, I haven't found google docs very nice for collaboration.


* Avoid Slack fights

  Slack can be great upto a point but discussions can devolve into heated arguments and regurgitation of the same points, much like keyboard warriors you come across on internet forums and WhatsApp groups. When this happens its better to get everyone with strong opinions into a meeting to have a more productive discussion and conclude.

* Build a shared understanding in the team

  Consider a developer that takes an approach to implement something and submits a pull request. However, other reviewers push a lot of feedback on design gaps and change suggestions - this can be demoralizing for the developer besides slowing down the team.

  Instead, for major changes, make sure that there is a shared understanding on the high level design before implementation.

  The same applies for QAs and Product too. This is where weekly iteration planning meetings to review work for next week are useful.


  <blockquote class="twitter-tweet"><p lang="en" dir="ltr">Pull requests work best when there is *already* a shared understanding of what/why/how. <a href="https://t.co/GgZrPqHvT6">https://t.co/GgZrPqHvT6</a></p>&mdash; Vishal Naik (@vishalmanohar) <a href="https://twitter.com/vishalmanohar/status/1370584611240046594?ref_src=twsrc%5Etfw">March 13, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


### What remote work demands from indiviuals


* Great work ethic

  The main concern for engineering manager regarding remote work is : "I am sure those with a good work ethic will work but there are a few people in the org who aren't just that committed and won't pull their weight if they know they aren't being monitored."

  While the office automatically creates a range of office hours to work, the freedom of working remotely means that you get to work whenever you want.

  However, this freedom also comes with a responsibility that you do work and are productive for a minimum set of hours everyday. If you are not able to for whatever reason, then the team must be informed.

  A great work ethic is a pre-requisite for remote work because a slacker will just take abuse of the system and become a drag to the whole team. Therefore, the org must also have mechanisms to monitor remote work  effectiveness and ensure perpetual slackers are weeded
  out.

* Shape your own environment to be productive
  When you are at an office, you are naturally in "work" mode and just seeing other people at work primes everyone else to work and be productive. So whether it is a boring task that just needs to be done, or you don't feel very motivated to work in the beginning of the day, you can still end up being productive thanks to the environment.

  However, when working from home you are on your own and need to create an environment that is great for work - whatever it means to the individual. For e.g. it might be setting up a quiet space or a workstation or reducing non work interruptions etc as much as possibly. Or, it might also be arranging for lunch which would otherwise have been provided at the office.

  Hanselminutes has a great podcast [on this](https://hanselminutes.simplecast.com/episodes/surviving-as-a-remote-tech-employee-with-jayson-j-phillips-G0lphUL1)

* Monitoring remote work

  "Managing by walking around" isn't possible when working remote obviously. When you are in an office, you can get a pulse of how well a team is working, who are the playmakers and who might need support.

  For e.g., you might see a senior mentoring a new person on the team or someone leading a design discussion or another person helping someone else troubleshoot something. Or you might just see the story wall and notice that a developer is stuck on a low complexity story for many days.

  With remote, the team will need to have mechanisms to compensate for the above.

  * Review code commits periodically.

  * Review pull request review time - if there are too many pending PRs in the queue its not a good sign. Maybe there is too much dependency on one lead developer to review the PR.

  * One-on-One meetings every week for new folks and atleast once in 2 weeks for the rest.

  * If there is too much back and forth on Pull requests and Jira tickets, its sign that there is a lack of shared understanding.

  * Ensure there is no single point of failure in the team for each aspect. For e.g. if the team relies on the same person everytime to troubleshoot a production issue or to perform infra changes, this needs to be addressed.

* Excellent communication skills

* Empathy

* Proactive Doer

### Hybrid
  Post Covid, whenever that happens, a hybrid approach where a team can work together for 2-3 days a week and then remotely for the remaining 2 days seems ideal.

  This way, a team can decide to have all their planned meetings and huddles that are suited for face to face on the office days and while benefitting from remote work on the rest.


### Interviewing for remote
