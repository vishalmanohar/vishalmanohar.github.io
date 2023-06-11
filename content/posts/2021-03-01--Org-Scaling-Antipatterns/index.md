---
title: Org Scaling Antipatterns
date: "2021-03-01T18:40:32.169Z"
template: "post"
draft: false
slug: "/posts/org-scaling-antipatterns"
category: "Software Development"
tags:
  - "swdev"
description: "Scaling from a 5-10 dev org to a 50-100 org can be messy if not calibrated."
---

(Incomplete draft)

Transitioning from Phase 1 of a start up where you have 1-10 member dev org to Phase 2 where you have 20-100+ dev org is a huge step and below are a few things I have observed in my consulting engagements.


## Phase 1
Phase 1 is the validation stage of the idea or building the product around a few early customers to demonstrate product market fit.

In this phase, you are ideally a small, nimble, self selected, high performance team.

During this phase, its all about iterating fast, onboarding customers quickly, building POCs for customer demos and delighting early customers with quick turnaround times.

There is no time for detailed requirement documents or iteration planning meetings, detailed estimation or the agile rituals and so the days can be unstructured (coding away a feature one moment to fixing a prod issue in the other to switching to a new priority for a customer demo for the next day) and there is a lot of ambiguity in the requirements.

But if you have been able to build a team of effective engineers from your network who are skilled in their craft and there is a high degree of trust, you can get away with not doing all of that and focus instead on building the product and getting that early traction.

In this phase, it is critical to have engineers that have the following attributes:

* **Founder mindset** - for e.g. is highly self motivated, understands the criticality of different tasks and prioritises accordingly, understands the WHYs etc.
* **Full stack engineer** - e.g. can work on frontend and backend with acceptable quality of work
* **Proactive Doer**
* **Strong Work Ethic**

## Phase 2

This is often the phase where the company has validated the product with early customers, raised more capital and its priority is to expand its capabilties to service even more customers and use cases.

This also means growing your dev org and adding more engineers to the team. But what got you till here won't get you there and recognizing this and adapting
is necessary to avoid [organizational debt](https://www.linkedin.com/pulse/problem-opportunity-organizational-debt-bharath-jayaraman/).

At this stage, things change dramatically for the dev org.
With each new member the lines of communication between members grow exponentially and beyond 5-7 poeople in the team, there needs to be hierarchy set up to bring some sanity.

![](https://cdn.shortpixel.ai/client/q_lossy,ret_img/https://getlighthouse.com/blog/wp-content/uploads/2015/07/lines-of-communication-stackoverflow-1024x953.png) - [source](https://getlighthouse.com/blog/developing-leaders-team-grows-big/)

There also needs to be derisking of individual dependency or [bus factor](https://en.wikipedia.org/wiki/Bus_factor) because the stakes are higher.

And then, there are usually compliance requirements to be met for bigger customers, need for UX consistency across the product, which means subject matter experts for SecOps and UX.

So after a certain point, the large team needs to be organized into smaller teams around modules. The roles and responsibilities need to be explicily called out and processes for everything from code repo branching to PR guidelines to QA and release process, to production support and access needs to be defined.

## Antipattern 1: Rampup before achieving PMF

## Antipattern 2: Hiring fast, firing slow

In Phase 1, the hiring is usually from close networks and there is no formal hiring process or interview. The people have already worked with one another and there is already trust established.

Anyone not pulling their weight is plainly visible and it is easier to let go.

However, beyond a size, the company needs to recruit second or third degree referrals and without sufficient vetting,

### Lack of standardized hiring process


### Short circuited process for referals

As the team are getting set up, given how hard it is to find good developers, sometimes you might hire someone who doesn't have the technical depth based on interview feedback but still don't want to lose them because maybe they can build those CRUD UIs or other areas in the app which don't need much tech chops.


## Antipattern 3: Feature Factory


## Antipattern 4: Structurelessness

A close knit small org doesn't need a lot of structure because there is a lot of trust and the communication lines are fewer. But beyond a team size of 10 and above, the lack of structure starts becoming an impediment.
Also suggested reading: [Tyranny of structurelessness](https://www.jofreeman.com/joreen/tyranny.htm)


## Antipattern 5: Lack of career ladder
