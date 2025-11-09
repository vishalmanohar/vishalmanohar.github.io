---
title: Building Software in the Age of AI
date: "2025-11-09T14:25:00.000Z"
template: "post"
draft: false
slug: "/posts/building-software-ai-age"
category: "Software Development"
tags:
  - "swdev"
  - "ai"
description: "What does AI leave for the vaunted software engineers who are staring at AI disrupting their own jobs?"
---

Up until a couple years back, software engineering was one of the most vaunted jobs. It became even more so during the covid bubble on the back of a digital and SaaS boom.
Salaries of even entry to mid level engineers skyrocketed during those days and demanding multiples of salaries just a couple years back.

AI has indisputably burst that bubble.

After all, no one predicted that coding, thought of as a highly analytical, deep thinking activity would be one of the first jobs to get disrupted by LLMs.
In hindsight of course, it makes sense that coding agents using LLMs would be great at coding: huge training data corpus. Programming languages impose syntax, there are tons of coding examples to learn from, LLMs learn the syntax and are able to apply an solution to a given context very well.

So well that now you can build software by just talking to AI without even having any programming experience. The era of "vibe coding" is upon us - it's just unevenly distributed.

And as has been claimed: 
>  The "de-nerdification of programming is now complete  - [link](https://vivekhaldar.com/articles/the-de-nerdification-of-programming/)


> But the nerd has a nostalgic feeling of loss at this impressive achievement. Someone called this feeling vesperance: “the solitary emotion of wistful recognition of the present as a fading era, tinged with anticipation for an unrecognizable, transformative future.”

As many, I was caught up in this feeling of "vesperence" for a while too. When you initially start using AI, it can be a sinking feeling to see how AI is able to zero-shot working solutions, debug using intricate implementation details you learnt the hard way etc.

LLMs immediately depreciate previously thought of as like intricate programming language syntax, knowledge of APIs, navigating a vast code base besides the coding itself.

But as you use more, you realise, it is a tool to lean in to. And once you do that more, you begin to enjoy using it to a point you don't want to write software without it. The more you use it you also become curious about how it works and start learning about Transformer, study the Build an LLM book, work through nano GPT etc. You also read the "Evolution of intelligence" book and marvel about how intelligence evolved in living beings.

Then you know it's not something to be feared and just a tool. At least, not yet.

You also realise how it is not a silver bullet for software development either. 
Jagged intelligence, catastrophic forgetting, lack of continuous learning and zero agency are serious gaps that mean that AI doesn't replace a software engineer.

But the nature of the job has changed. AI certainly eats a lot of tasks that a programmer has to do. But that yields the human more time to work on higher leverage things.

So, where does that leave the software engineer? What skill will become more important?

But before that, how is AI most effective now:

### AI as a pair programmer

With AI coding agents like Claude Code, Codex etc taking much of the heavy lifting of writing the code with delightful developer experience, the job of the engineer shifts to becoming a navigator in a pair programming set up.

Typically, a "pair programming" set up involves a driver who has the control of keyboard and the mouse. The driver implements the coding requirement, fixes compiler errors, refactors etc  and the navigator guides, thinks about bigger picture, abstractions, design, non-functional requirements, how the solution fits into the context etc.

With coding agents, the developer role shifts to navigating or steering the AI to a desired solution while using its inputs to make the right judgement calls.

AI can arguably build the entire solution given a PRD and it might work for a lot of use cases but given its limitations, you still need a human in the loop to review and guide the solution.


### AI as an intern or junior developer

Any work you can define and scope well and assign to a junior developer can be done by an AI. Basically, these are tasks where there is enough detailing, there is low ambiguity and easily verifiable.


### AI as a sparring partner

When you want to analyse tradeoffs, discuss multiple approaches to a solution, LLMs with their information retrieval and reasoning can be a good way to bounce ideas, explore different solution spaces before settling in.


## Role collapse

AI is clearly "lowering the floor and raising the ceiling". It reduces the entry point for you to pick up tasks and can raise the quality of the output if wielded correctly as well.

As I take up tasks, the roles that were created earlier to un-bottleneck the slowest task of actually writing software namely: business analysis, UI design, armchair software architecture is collapsing.

Effective teams will have Product managers vibecoding POCs and mock ups for early customer feedback while developers will require lesser spoonfeeding of detailed tickets with AI filling in the gaps.

This can be seen in orgs which now have a "forward deployed engineer" role that works with the customer and "business" directly, identifies problems and then builds the solution like AI agents using AI.


## Durable Skills
So, what are the durable skills to build on in the age of AI assisted software development? Those will be skills that make the human complement well with AI.

Code monkeys who just get by glueing APIs and slinging UI code will be eaten by AI.

Instead, deep skills like critial thinking and analytical skills, foundational knowledge of algorithms, system design, breadth of experience with various architectures, design patterns, learnability etc will become premium - because these will still be required to collaborate effectively and draw the optimal output from AI. As Kent Beck says ["AI is an unpredictable genie who grants wishes"](https://newsletter.pragmaticengineer.com/p/tdd-ai-agents-and-coding-with-kent) and you need to be careful and thorough with what you wish for.

While anyone can vibe code a tool for personal use, a software that will be used by thousands of organizations or millions of users will have different contexts and considerations - blanks that can only be filled in by someone who knows what they are building and how to wield AI.


## T-shaped is back

> A T-shaped engineer is a professional with deep expertise in one field (the vertical bar of the T) and a broad knowledge base across many other disciplines (the horizontal bar). This combination of specialized knowledge and versatile skills allows them to tackle complex problems, collaborate effectively, and adapt to a constantly changing technical landscape. They are highly valuable in cross-functional teams, as they can contribute to their area of expertise while also helping with tasks in other domains, preventing project bottlenecks.  

While the boom cycle rewarded even shallow or surface level skills, AI forces people to raise their own bar or be ever vulnerable to the next job cut.

Proficiency in two or three programming language systems, putting a system in production, baking in observability, reliability, performance, systems design all become more important since AI has eaten the low hanging fruit.

While chatting with an AI can give an illusion of picking something fast, real learning happens when you apply a concept in practice and learn from feedback.
So, the "10,000 hrs" would still hold good. AI might compress this by making the feedback loop faster and bring better learning examples but you still need to put in deliberate practice - leveraging AI when it makes sense.

---

In short, this is a very exciting time. Just as Software engineering was becoming boring with systems like cloud native architectures, platforms, tools and frameworks maturing over the recent years and AI provides the next big leap both in how software is built and what it can do.
