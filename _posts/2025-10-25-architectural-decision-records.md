---
title: "The importance of documenting architectural decisions"
date: 2025-10-25 T21:14:30
categories:
  - planning
tags:
  - planning
  - process
  - architecture
excerpt_separator: <!--more-->
---

Decision-making can be complex. It involves weighing up different options and considering various tradeoffs. The rationale for what is decided is not always documented. This makes decisions harder to understand and harder to change later and can determine the success or failure of a project.

In my previous role as a consultant in machine learning and data engineering, I was generally hired to build something new in what was (at the time) unchartered territory. Machine learning was just taking off and many companies were unsure how to use it and had neither the infrastructure nor the data to support it.

It was my job to design and build data pipelines for training and running machine learning models that would output useful information for use in making business or engineering decisions -- either in real time or on a schedule.

Unless the company was a brand new startup, there was already existing business logic in place to help with these decisions, which usually involved a lot of manual work to analyse data and create reports and/or dashboards. Part of the drive to implement machine learning was to automate a lot of this and free up time for working on other problems that could not be automated.

While documentation existed for how things were currently done, what was often missing was documentation for **why** things were done a certain way.

There were usually two camps -- one that wanted to stick with the current way of doing things and were deeply sceptical of "black box" models (often domain-experts who crafted the existing logic and analysed the data) and another that wanted to embrace these models, as long as they could be verified and validated (usually the people making the decisions). A lot of friction, miscommunication and politics resulted from this, which is a shame since domain expertise is critical for the success of machine learning projects.

One thing that would have helped both sides reach a mutual understanding would have been a written record of why certain choices were made in the first place. Most likely, there were very good reasons for the choices that were made initially as well as risks and limitations that were accepted at the time. But technology evolves rapidly and those same people may have chosen differently in today's technology landscape (or not -- they may have specific knowledge that is not obvious to others).

When the rationale (and pros and cons) for earlier choices are forgotten there is no way to know whether they are still good choices today. This means that in the worst case, people are either afraid of changing something in case it breaks (and risk the project becoming hard or cotstly to maintain, outdated and/or outcompeted) or change something that should not be changed and break it (and waste time and energy implementing and then reverting it, potentially putting the whole project in jeopardy).

Inspired by the [decision-making process for software development at SKAO][adr-skao] (where I now work), I've recently been learning about [architectural decision records (ADRs)][adr]. ADRs have been around since the 90s and provide a solution to the problem of lost knowledge. They were popularised in [a 2011 blog post by Michael Nygard][nygard]. An ADR is a structured way to document rationale for software design choices for your future self and future colleagues. It can include all the alternatives you considered and any known risks. When someone new to your project comes in and wonders why things are done a certain way you can point them to these records. If they disagree then they have the complete history available to them to confidently propose a new ADR to change the earlier decision. You can also use them as context for AI assistants to help them make better recommendations.

As part of [my python project template][template], which I've created to streamline [starting new open source projects][template-post], I have an [ADR on using ADRs][adr-001], which lays out my rationale for using them, the alternative solutions I ruled out and how I will adopt them in practice. I have also added [a template for new ADRs][adr-template].

Documenting decisions in this way would also be useful in other domains -- I ran into similar problems when working in a molecular biology lab. Everyone followed a particular protocol and no one I worked with had tried to optimise any of the steps. Why it was done this way was knowledge that had been lost over time and no one wanted to change the way it had always been done... Deciding what research topic to work on is another example. I documented my rationale for using a decision matrix in [an earlier post][what-to-work-on] but I could have used something like an ADR for this. 


[adr]: https://adr.github.io/
[adr-skao]: https://developer.skao.int/en/latest/policies/decision-making.html
[adr-template]: https://open-research.gemmadanks.com/python-project-template/architecture/adr/template/
[adr-001]: https://open-research.gemmadanks.com/python-project-template/architecture/adr/001-use-architectural-decision-records/
[nygard]: https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions
[template]: https://github.com/gemmadanks/python-project-template
[template-post]: https://open-research.gemmadanks.com/tutorials/python-project-template/
[what-to-work-on]: https://open-research.gemmadanks.com/planning/choosing-research-topic/