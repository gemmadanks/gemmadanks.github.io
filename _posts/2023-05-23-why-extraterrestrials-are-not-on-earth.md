---
title: "Why are extraterrestrials not on Earth?"
date: 2023-05-23 T14:20:00
categories:
  - literature
tags:
  - research
  - astrobiology
  - technosignatures
  - literature
  - summary
  - seti
---

After a series of papers on searching for communication signals from extraterrestrial civilisations {% cite  bracewellCommunicationsSuperiorGalactic1960  Cocconi1959  dixonSearchStrategyFinding1973  drakeProjectOzma1961  dysonSearchArtificialStellar1960  hoernerSearchSignalsOther1961  kardashevTransmissionInformationExtraterrestrial1964  ProjectCyclopsDesign1972  schwartzInterstellarInterplanetaryCommunication1961  %}, Michael Hart at NCAR in Boulder, Colorado, published a paper in 1975, in the Quarterly Journal of the Royal Astronomical Society, arguing that the only reasonable explanation for why extraterrestrials have not travelled to and colonised Earth is that they do not exist {% cite  hartExplanationAbsenceExtraterrestrials1975  %}. 

This paper was reportedly the first formal examination of the now famous [Fermi Paradox][fermi-paradox] (named after a remark made by Enrico Fermi in 1950 during a lunchtime conversation: if there are so many extraterrestrial civilisations and they can travel through space, where are they all?), although Hart did not refer to Fermi. 

Here are my notes on Hart's 1975 paper. You can find my notes on other classic SETI papers in my [roundup of the technosignatures literature][technosignatures-literature].

I also created a [Jupyter notebook][jupyter-hart] to explore these ideas further.

## Fact A
Extraterrestrials are not present on Earth (Hart called this 'fact A'). This piece of empirical data requires an explanation. Many had been put forward at the time the paper was written but Hart argued that they were all insufficient to explain why no alien civilisation anywhere in the galaxy, at any time in its history, had travelled to our Solar system and settled here. He proposed that the best explanation is that extraterrestrial civlisations don't exist, making the search for them a waste of time and money. 

## Why aren't extraterrestrials on Earth now?
Hart grouped alternative explanations for fact A and used the rest of his paper to state his reasons for rejecting them all.

### Physical explanations: they can't get here
The stars are light years away and travelling at speeds fast enough to make the journey in a reasonable time requires a lot of energy. It is also dangerous. 

#### The travel time is too long
Hart proposed several possible solutions to the problem of long travel times between the stars:
- Put the passengers into suspended animation or freeze them for the journey
- Use robots to pilot the spacecraft and send zygotes
- Plan a multi-generation mission
- Extraterrestrials have much longer lifespans than humans: the trip might be relatively short for them

#### It is not possible to carry enough (chemical) fuel
The high energy demands can be solved by using nuclear power and travelling at a tenth of the speed of light, which would use nine times the mass of the payload in fuel.

Energy requirements of a ship can also be reduced further:
- Refuel from an auxilliary ship
- Collect hydrogen atoms along the way
- Improve engine efficiency
- Reduce speed
- Use a method of propulsion other than rockets
  
#### It is too dangerous
Hart dismissed arguments that cosmic rays, meteoroids, the damaging physiological effects of weightlessness and other unknown dangers as not prohibitive for space travel, given that [Apollo 11][apollo-11] and [Skylab][skylab] missions had been successful.

### Sociological explanations: they don't want to
Arguments that extraterrestrial civilisations are not interested in space travel might explain why one particular civilisation at one particular time in its history may not explore the galaxy but, Hart argued, they cannot explain why no civilisation at any time in its history doesn't. Civilisations differ and they change over time. This is true for any sociological explanation, including the explanation that civilisations destroy themselves before they manage to leave their planet (he noted that humans have not destroyed themselves and we should not develop a theory that predicts most extraterrestrials will behave in the opposite way to us).

Hart also stated that we can never accept a sociological explanation since there is no way to test its validity. 


### Temporal explanations: they haven't had time
Hart conducted a thought experiment to reject this argument. 

If we were the first civilisation in the galaxy and we could travel at one tenth the speed of light and not take breaks, we could colonise the galaxy in 650,000 years. Allowing for double this time, Hart argued that unless a civilisation began exploring space less than 2 million years ago they should already be here (since the galaxy is approximately 10 billion years old and it is unlikely that all advanced civilisations take so long to start exploring).


### They have been here but didn't stay
Any argument that extraterrestrials have been here but did not stay requires an explanation that applies to all civilisations at all times and so suffers from the same problem as any of the sociological explanations.

## Summary
Hart concluded that since there are no extraterrestrials on Earth there cannot be thousands of them scattered throughout the galaxy. If there were so many one of them would have reached us. There is no alternate explanation that can be applied to all civilisations at all times in their histories. Based on this, Hart also argued that an extensive search for communication signals is probably a waste of time and money and that our descendants will probably eventually colonise the galaxy. He proposed that future research may provide the answer to why intelligent life has evolved first on Earth.

It was interesting to read a paper that had a pessimistic perspective compared to a lot of optimism from others at the time. It was perhaps optimistic, however, to assume that even one technologically advanced civilisation would survive long enough, and have enough resources, to colonise an entire galaxy.

## References

{% bibliography --cited %}

[apollo-11]: https://www.nasa.gov/mission_pages/apollo/missions/apollo11.html
[fermi-paradox]: https://en.wikipedia.org/wiki/Fermi_paradox
[jupyter-hart]: https://github.com/gemmadanks/technosignatures/tree/main/fermi-paradox
[skylab]: https://www.nasa.gov/mission_pages/skylab
[technosignatures-literature]: https://open-research.gemmadanks.com/literature/technosignatures-literature-roundup/

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>