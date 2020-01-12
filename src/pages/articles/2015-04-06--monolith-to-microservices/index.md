---
title: Monolith to Microservices
date: "2015-04-06T22:40:32.169Z"
layout: post
draft: false
path: "/posts/monolith-to-microservices"
category: "Software Development"
tags:
  - "swdev"
description: "Reflections on a re-architecutre from monolithic app to microservices"
---

I was reading Building Microservices recently and couldn't help but draw parallels to a recent project where we had to work on a monolithic application that ultimately evolved into multiple mini applications that allowed different teams to independently deploy their apps. 

### Single team, Large codebase

When we started out it was a single large team of atleast 10 dev pairs working off a monolithic code base but different isolated features of the application. While being a single team affords a lot of benefits like easier communication, keeping everybody in sync, better rotation and skill mix, it doesn't work very well especially for junior members in the team who will find it difficult to focus when they have work on different parts of the application on a continuous basis. This negatively effects code ownership and motivation. I initially didn't think splitting into smaller teams was a good idea mostly because I thought it would add a lot of communication overhead, hamper cross pollination etc. but now, I think doing so was critical for project delivery, team happiness and code quality.

Of course, identifying the seams to divide the teams along, team mix etc. are all important factors to consider before dividing teams. Having the separate teams in the same location, common project showcase meetings and tech huddles should help keep everybody across teams aligned in the larger direction.

### Smaller teams, separate codebases

Splitting into smaller teams helped in lot of  ways but every team working on the monolith code base still had some critical problems: 

Ownership of overall application code was not clear. 
Difficult to reason about code in large code bases
Different coding patterns emerged in each team and it was difficult to consolidate
Builds were slow with the large code base, more tests etc.
A broken build would block every team
A large automated functional test suite that was ignored because of lack of ownership

These are typical issues with large monolithic codebases and a side effect of Conway's Law.


Splitting the monolith into smaller independent code bases along functional lines and team structure helped a great deal. We then had a much smaller code base to reason about, much faster builds, test pipelines that were specific to what the team was building and a consistent coding style within the same codebase.

### Microservices

Although we had split the codebase along the lines of a team, the deployment of these modules were still as part of the monolithic application. This coupled the release of team specific features with that of the monolith and still retained a significant overhead in deploying software because you need all these different teams to coordinate and sign off on a build and deploy it.

While a lot of focus in adoption of CD is lent towards Dev Ops automation, I think having a modular architecture with independently deployable software units is the most important piece because without this you are still stuck with all the  testing and coordination overhead required to deploy the monolith.

Dividing the monolithic app into smaller independently deployable mini-apps (fashionably called Microservices) helped address this.

Teams now have autonomy on releasing software features without being coupled to any other team and have better ownership of their features.
