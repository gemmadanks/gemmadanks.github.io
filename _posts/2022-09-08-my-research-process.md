---
title: "The benefits of process mapping and my research process"
date: 2022-09-08 T14:25:00
categories:
  - planning
tags:
  - about
  - process
  - planning
excerpt_separator: <!--more-->
---

For several years I worked as a consultant in a large engineering firm, building advanced machine learning models for predictive maintenance of their equipment. During this time I was often asked to formally document (or map) the processes I was following when developing and deploying models. 

A process map is simply **a visual overview (flow chart) of a set of activities** - in this case, how to go from raw data to a model fit for real-world use. 

Creating these maps was time-consuming to start with but it had enormous benefits in the long run (more on that below) and I found it so valuable in the end that I also took this approach in other projects outside of engineering and I am now using it to map and optimise my research process. I recommend using it for any set of activities that is repeated and where efficiency or clarity is important.

## How to map a process
1. Identify all events, activities, tasks, decision points, inputs, outputs, resources and people involved
2. Order and connect activities and decision points into a sequence
3. Group tasks into sub-processes where appropriate
4. Draw up and annotate a flow chart (or several if sub-processess are involved) - use standardised symbols for ease of sharing with others (I am using the [Business Process Model and Notation (BPMN)][bpmn]):
   - Circles = events
   - Rectangles = activity (dashed outline if this is a subprocess)
   - Diamonds = decision points
5. Identify any gaps or unclear tasks and fill these in
6. Share with stakeholders and respond to feedback
7. Regularly review, improve and update the process

## Benefits of process mapping
- Complex processes can be communicated to stakeholders in a format that is easy to understand (e.g. how do you go from raw data to a model that alerts engineers of a problem) - this was critical in my engineering projects
- Important decision points are documented and easily referenced (e.g. is this model good enough to deploy?)
- A process map provides a framework for discussion with domain experts (e.g. what model outputs are the most useful for an engineer)
- New team members can be onboarded quickly (the map puts the project as well as the source code in context)
- It is easier to spot bottlenecks, activities that don't add value and areas with room for improvement or simplification (e.g. this step takes time because it requires detailed validation by a domain expert)
- The order of activities is standardised, which improves efficiency (e.g. do not optimise the model architecture until you have agreed on the outputs with the engineers)
- All team members gain a clear understanding of the entire process even if they are only working on one task
- Rabbit holes and time spent on unnecessary incremental improvements are avoided (e.g. if the error is below this threshold it is good enough to deploy now, since this provides more value than waiting for a better model) - this was the biggest difference in mindset I experienced working in industry vs. academia

## My research process

Here is the result of a morning spent mapping my research process - a flow diagram that starts with the event 'field of research chosen' and ends with the event 'publication accepted' and iterates for endless opportunites for discovery!

I have coloured the arrows to show the shortest path (green), the paths involving additional learning or growth (blue) and the paths that lead to delays and should be avoided if possible (red).

Over time, I will return to this diagram and revise it. I will also create maps for the sub-processes (activities with dashed outlines) as I go along.

![My research process](/assets/images/process-research.jpg)

This is essentially the process I settled into when I was a senior postdoc, managing my own projects. It is based on my own experience in molecular biology and bioinformatics. Overall, it is a fairly standard way of conducting academic research but my process has evolved somewhat over the course of my career leading to two main tweaks compared to how I started.

###  Hypothesis-driven research only

At the beginning of my research career (PhD and first postdoc) I did a lot of exploratory research and only later focussed on formulating and testing specific hypotheses (which emerged from the exploratory work). I much prefer the hypothesis-driven appproach - diving into data looking for patterns quickly becomes (for me at least) overwhelming and frustrating without a specific question to answer and it can lead to a lot of wasted effort. 

From now on, I will only move forward if I have a specific question in mind. 

### Start at the end
The biggest shift in how I worked happened during my second postdoc when I also had my second child. Juggling a baby, a toddler and my research meant I needed to be much more efficient. I decided to eliminate all activities that would not lead to the end goal, which in academia is always publications - as many as possible in journals with as high an impact as possible. This is how researchers are judged - 'publish or perish' is the reality.

So I started at the end goal - outlining the paper. I already had a hypothesis I wanted to test so I started with what results (figures and statistics) would allow me (and the scientific community) to accept or reject my hypothesis. Then I worked backwards:
- What data would I need to obtain these results?
- What experiments would give me this data?
- What resources (people, time, skills, equipment, reagents) would I need for these experiments?

I then sketched the figures and wrote an outline for the methods and results sections. I listed the important background topics in the introduction. 

The gaps in this paper outline, and only the gaps, formed the tasks for me to complete. This included literature reviews and designing and conducting experiments and analyses (both wet and dry lab). 

This saved a lot of time and made my work much more efficient and focussed. It turned out that the final step - getting the paper published - was the main bottleneck, which is not uncommon in the research process! You can see the final result (open access) [here][pub-oiko-mtor].

For my open research I will use the same paper-driven approach since I do think a paper is a good tool for focussing my efforts as well as providing a good summary of the research (with the benefit of hindsight), giving others the shortest path to my results. The main difference will be that I also publish my output at each step along the way towards publication.

## Share your thoughts
Do you have any thoughts on mapping processes or the research process? Let me know in the comments below!

[bpmn]: https://www.bpmnquickguide.com/view-bpmn-quick-guide/
[pub-oiko-mtor]: https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-019-6277-x