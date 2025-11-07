---
title: "My software development process"
date: 2025-11-07 T09:47:00
categories:
  - planning
tags:
  - about
  - process
  - planning
  - software
excerpt_separator: <!--more-->
---

I am a big fan of process mapping. I used it a lot in my role as a consultant in machine learning and have previously written about [mapping out my research process][my-research-process]. It helps to clarify muddy waters when it comes to how things are done in practice. Lately I have been thinking about the software development process and wanted to map this too. This will give me a handy reference for when I am starting new projects and encourage me to reflect on how I can improve my software development process, how it relates to my research process and how best to integrate the two.

This post is a summary of my software development process. I will use it for working on my first software package for technosignatures research. As I execute each step I will document more details on the process as well as my results and reflections.

I am also experimenting with ([mermaid][mermaid-docs]) for creating the final flow chart.

## My software development process

Here is the result of a few evenings mapping my software development process using the mermaid live editor. I have used a flow diagram that starts with the event 'Domain chosen' and ends with 'Continuous Delivery Cycle'. It results in working software that can be iterated upon in endless opportunites for development! For the steps inbetween, I have cherry-picked the practices that I have found most useful in my career so far, new practices I want to try and practices I want more practice in. As I follow this process, I will refine it and reflect on what worked and what didn't.

I have outlined more details on the main steps below.

<pre class="mermaid">
flowchart TD
  START@{ shape: circle, label: "Domain chosen" }
  DDD@{ label: "Explore Domain" }
  OUT_DM@{ shape: lean-r, label: "Domain map" }
  OUT_GL@{ shape: lean-r, label: "Glossary"}

  PRIORITISE_PROB@{ label: "Identify Key Problems" }

  IM@{ label: "Map Impacts" }
  OUT_IM@{ shape: lean-r, label: "Impact map"}

  PRIORITISE_DEL@{ label: "Prioritise Deliverables" }

  REQ@{ label: "Elicit Requirements" }
  LIST_BDD@{ shape: lean-r, label: "BDD scenarios" }
  OUT_UT@{ shape: lean-r, label: "Utility tree" }

  DOCS@{ label: "Outline Docs" }
  PROTO@{ label: "Prototype" }
  ARCH@{ label: "Evolve Architecture" }
  
  ARCH_VIEWS@{ shape: lean-r, label: "Architecture Views" }
  ARCH_DECISIONS@{ shape: lean-r, label: "ADRs"}

  CD@{label: "Continuous Delivery Cycle"}

  OUT_SW@{ shape: lean-r, label: "Working Software" } 

  START --> DDD --> OUT_DM & OUT_GL 
  DDD & OUT_DM  --> PRIORITISE_PROB --> IM --> OUT_IM
  IM & OUT_IM --> PRIORITISE_DEL --> REQ
  REQ --> LIST_BDD & OUT_UT
  REQ --> DOCS & PROTO
  PROTO & DOCS & REQ & OUT_UT--> ARCH
  ARCH --> ARCH_VIEWS & ARCH_DECISIONS
  ARCH & ARCH_VIEWS & ARCH_DECISIONS --> CD 
  LIST_BDD --> CD
  
  CD -.-> |Learn| DDD
  CD -.-> |Evolve| ARCH
  CD -.-> |Refine| REQ
  CD -.-> |Evaluate| IM
  OUT_GL --> REQ
  OUT_GL --> ARCH
  OUT_GL --> CD
  CD --> OUT_SW --> CD
</pre>
<script src="https://cdn.jsdelivr.net/npm/mermaid@11.12.1/dist/mermaid.min.js"></script>

### Explore Domain (DDD)
The first step is to identify what problem to solve. I have previously described the [method I used to choose a research topic][choose-topic]. I will use a similar approach to choosing a problem to solve (by developing software) within that topic. This means first exploring the domain, creating a domain map and then prioritising any problems identified by ranking them by a) impact b) tractability c) neglectedness and d) personal fit. That way I will develop something that: solves an important problem; is within my capabilities and interest; and not many others are working on. 

As part of this [domain-driven design (DDD)][ddd] approach, I will also generate a glossary of terms that I will use for aligning to the domain language when designing and coding my software. This will make communication with domain experts and users much easier (this is one of the hardest parts of developing software in a domain you are not expert in yourself and can make or break a project).

### Map Impacts
After identifying the key problems, the next step involves formulating them into a set of goals and mapping these to **actors** (the people or entities affected), **impacts** (behavioural changes) and **deliverables** (the solutions that will define user stories -- see below). This map provides many routes to tackling a problem with measures of success (defined by the impacts) that can be used to evaluate progress towards the goals. This is an approach I would like to gain more experience in.

### Prioritise deliverables
I will prioritise deliverables by mapping them onto a value vs. effort chart and rank by value/effort, taking quick wins (high value, low effort) first to build momentum.

### Elicit Requirements
Once I have a set of top deliverables, I will spend some time specifying requirements for each. These will include:
- **Functional requirements** (what should the software do?) that I'll formulate as **user stories** ("As a <user role>, I want <some capability> so that <reason or benefit>") that I can use to derive **[behaviour driven development][bdd] scenarios** ("Given I have <something> when I <do something> then <something happens>") that will form the basis for BDD tests. I have used the BDD approach before and found it very useful.
- **Non-functional requirements** (how should the software do it?) that define **quality attributes** (such as maintainability or scalability) that I can use to derive **quality attribute scenarios** ("When <stimulus> occurs, and the system is in <context>, the system shall <response> with <measure>" for standard use cases and cases covering both expected and unexpected changes), some of which can be used to derive automated tests. As part of this step I will create a **utility tree**. This maps quality attributes to concrete testable quality attribute scenarios. This is one of the practices in the [Architecture Tradeoff Analysis Method][atam] that I want to practice and learn more about.

## Outline documentation
This is where the process gets a little unconventional compared to what, in my experience, is the usual way of developing software. In most projects I've worked on in the past, we've taken user stories and gone straight to coding. But this sometimes led to implementing something that wasn't quite what the users wanted and having to refactor, rewrite or build in unnecessary complexity later. I want to try documentation-driven development as a way of clarifying what the final result should be and streamlining the implementation.

This mirrors the [research process][my-research-process] that I landed on as I gained experience as a postdoc -- I started to outline the paper before doing any experiments. So, for my software projects, I will first write the README, then outline the docs. I will use the [diataxis][diataxis] framework and start with some explanation followed by tutorials and how-to guides. That way, all I have to do is design the software to do what the documentation says it does. I will iterate on these docs, ideally getting feedback from users, until they represent what I have to implement at a high level.

### Prototype
Inspired by design thinking I will also do some prototyping alongside writing the documentation outline. This will ensure that the final outcome will have the desired impact -- i.e. it will be something that a) solves a problem that people care about and b) people actually want to use.

I will sketch some designs for the user-interface and generate example outputs to check that this is what a user actually needs and wants to use. This might include the design for a dashboard with mock plots, the outline of a notebook, a mock log file or a simple script that includes a call to a CLI.

### Evolve Architecture
By this stage I'll have a clear idea of what the software will do and how a user will interact with it. I'll have an outline for the documentation and some basic prototypes for the user interface and outputs. The next step is to decide how the software will achieve this functionality given all the forces at play and the quality attribute scenarios I defined earlier in the process. For this I will research and select candidate architectural pattern that seem to best fit then I'll create architecture views using the [C4 model][c4-model] (Context → Container → Component → Code) for each. I'll then identify sensitivities, tradeoffs, and risks to create a tradeoff matrix that I can use to make decisions, documented in [Architectural Decision Records][adrs] and updated architectural views.

I plan to learn more about evolutionary architecture to ensure that the architecture design an iterative process and in a feedback loop with the continuous delivery development cycle (i.e. it evolves along with the code) with automated tests using fitness functions to ensure the code aligns with architectural decisions.

### Continuous Delivery Cycle
This step is where I write the code, starting with a minimal viable product (MVP) and creating a scaffold based on my architectural views. 

I plan to follow [Extreme Programming (XP)][xp] practices as far as possible, with test-driven development (TDD), short iterations, (AI) pair programming, continuous delivery and small, frequent releases. The whole process then becomes iterative in order to respond to change.

I will evaluate progress based on my impact map, refine the requirements and evolve the architecture regularly. I will also add anything new I've learnt about the domain to my domain map and adjust the impact map as needed.

### Reflections on using Mermaid
I used the mermaid live editor to create my software development process map and found it a really nice tool to use and much more efficient than other tools I've used before (including miro, omnigraffle, powerpoint). There are lots of options in mermaid that I haven't explored yet and there are some issues with the way the layout is rendered so I'll continue experimenting with it (including for my software documentation and architecture views).

There are also several advantages of having diagrams as code that I like, including how much easier it is to see changes using version control and how it makes them more AI-friendly and so can be used as context for AI assistants/agents that can both help improve the diagrams themselves and make better recommendations when assisting with code development (since you can point them to your process to show how you want to work).

## Share your thoughts
Do you have any thoughts on mapping processes or the software development process? Let me know in the comments below!

[adrs]: https://open-research.gemmadanks.com/planning/architectural-decision-records/
[atam]: https://en.wikipedia.org/wiki/Architecture_tradeoff_analysis_method
[c4-model]: https://c4model.com/
[choose-topic]: http://127.0.0.1:4000/planning/choosing-research-topic/
[ddd]: https://martinfowler.com/bliki/DomainDrivenDesign.html
[diataxis]: https://diataxis.fr/
[my-research-process]: https://open-research.gemmadanks.com/planning/my-research-process/
[mermaid-docs]: https://mermaid.js.org/intro/
[xp]: http://www.extremeprogramming.org/rules.html