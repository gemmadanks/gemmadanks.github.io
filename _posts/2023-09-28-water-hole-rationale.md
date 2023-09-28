---
title: "Rationale for the water hole"
date: 2023-09-28 T11:10:00
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

Searching the 'water hole' for extraterrestrial signals had already been proposed nearly a decade earlier as a result of the [1971 Cyclops Project][project-cyclops-notes-part-i] {% cite  ProjectCyclopsDesign1972  %} but in 1979, several navigational satellites were planned that would create noise in this frequency band. In response, co-director of the Cyclops project, [Bernard Oliver][bernard-oliver], published a paper titled "Rationale for the water hole" {% cite  oliverRationaleWaterHole1979  %} to make the case for keeping the water hole free from interference so that we are not "blind" to the signals from other technologically advanced civilisations. 

> It would be a bitter irony if the desire to know exactly where we are at all times on Earth were to prevent us from ever knowing where we are with respect to other life in the Galaxy.

Here are my notes from reading this paper.

You can find my notes on other classic SETI papers in my [roundup of the technosignatures literature][technosignatures-literature].

## What is the 'water hole'?
The water hole is a frequency band in the electromagnetic spectrum that lies between the hydrogen line (1420 MHz) and the hydroxyl radical emission line (1662 MHz): hydrogen (H) and hydroxyl (OH) are the dissociation products of water (H$$_2$$O), which is essential for all life that we know about. 

The hydrogen line is the frequency of radiation emitted by the reversal of the spin of the electron (a spin-flip transition) in neutral hydrogen atoms (corresponding to a wavelength of 21 cm). Radiation at this frequency can penetrate interstellar dust and since hydrogen is the most abundant element in the universe it is likely to be detected by any technologically advanced civilisation. It was the region around the hydrogen line that was originally proposed and targetted by early SETI researchers when other emission lines had not yet been discovered {% cite  Cocconi1959  dixonSearchStrategyFinding1973  drakeProjectOzma1961  %}. 

Bernard Oliver and the other members of the [Cyclops Project][project-cyclops-notes-part-i] {% cite  ProjectCyclopsDesign1972  %} later suggested that the region between the hydrogen and hydroxyl lines forms a poetic place for water-based life to meet: life on Earth gathers at water holes.  

## Why focus on the 'water hole'?
Oliver argued that the basic premise leading to the water hole is that a civilisation wishing to make contact with others will choose the least expensive method that guarantees success. 

### Radio waves are the most efficient means of communication
Like others before him {% cite  Cocconi1959  drakeRADIOSEARCHINTELLIGENT1965  hoernerSearchSignalsOther1961  ProjectCyclopsDesign1972  %}, Oliver excluded communication via space travel or probes on account of the time and energy they would require. This left communication via radiation. Oliver listed two main requirements that this radiation must have in order to detect it as an artificial signal: it must be significantly stronger than background radiation and have some property that is not found naturally. He also listed seven other properties:

- Requires the least radiated power
- Not absorbed by the interstellar medium or atmospheres
- Not deflected by galactic fields
- Readily collected
- Efficient generation and detection
- High travel speed
- Normally radiated by technological civilisations

This ruled out any particles with mass (since they would travel slowly and require too much energy to generate) or charge (these would be absorbed and/or deflected). It also excluded gravitons and neutrinos since they are not readily collected nor efficiently or normally radiated. Only low energy photons (radio waves) met all the criteria (they can be modulated such that they are not confused with natural sources).

### Maximising the signal to noise ratio
There are three contributions to background noise in received signals, which are similar everywhere in the galaxy:
- Synchrotron radiation (produced by electrons travelling in spirals along magnetic field lines) (at frequencies < 1 GHz)
- Cosmic microwave background radiation (produced just after the big bang)
- Quantum noise (at frequencies > 60 GHz)

These define a quiet region from 1 - 60 GHz (the free-space microwave window). 

On the surface of an Earth-like planet there are additional sources of noise from molecules in the atmosphere re-radiating noise:
- Water vapour (around 22 GHz)
- Oxygen (around 60 GHz)

These further narrow the window to 1 - 10 GHz (the terrestrial microwave window). This is where the detectable received power is at its lowest.

### Other advantages of the microwave window
Oliver listed further advantages of focussing the search in the (low) microwave region.
- Lower cost per unit of collecting area
- Greater collecting area for the sharpest usable beam
- Greater freedom from H$$_2$$O and O$$_2$$ absorption
- Higher beacon powers easier to achieve
- Narrower bandwidths are possible

### Accounting for Doppler drift
Planetary rotations and revolutions cause a change in the frequency of a signal. The motion at the receiver end can be corrected for but is more difficult at the transmitter end if the signal is omnidirectional (although ways to do this had been proposed {% cite  dixonSearchStrategyFinding1973  %}). 

Oliver showed that the optimum bandwidth for a signal (too high and there is too much noise; too low and it will be not be received) increases in proportion to the square root of frequency. Correcting for this narrows the quietest region of the microwave window to a 2 GHz region containing the water hole.

### Chauvinistic and romantic nonsense?
The minimum noise after correcting for Doppler drift occurs at 1.5 GHz but, Oliver argued, this does not increase much within a 2 GHz band. This is too wide to search or to keep free from interference and there is no technical reason to prefer a particular frequency over another. It does, however, include the water hole proposed by the Cyclops team due to water's significance for life on Earth. 

Oliver admits that it is both romantic and "chauvinistic to water-based life" but argued that it is not nonsense. We can expect water to be a common feature of habitable planets and he stated that "water-based life is almost certainly the most common form and well may be the only (naturally occurring) form". Today the search for life on other planets is largely driven by the presence of conditions suitable for liquid water.

Oliver also argued that romance itself may be "a perception peculiar to intelligence" and that intelligent extraterrestrial life may also perceive it.

## Summary
In this 1979 paper, Bernard Oliver re-examined the case for focussing our search for signals from extraterrestrial intelligence on the 'water hole', a region of the electromagnetic spectrum bound by the emission lines of hydrogen and the hydroxyl radical. His main motivation was to argue for protecting this region against interference from e.g. navigational satellites. He concluded that, while there may be reasons for choosing another region of the spectrum or another method of communication that we don't know about yet, this should not stop us from searching the water hole since "progress requires us to proceed on the basis of what we know, and not forever wait for something now unknown to be discovered".

## References

{% bibliography --cited %}
[bernard-oliver]: https://www.seti.org/bernard-m-oliver-1916-1995
[cocconi-morrison-1959-notes]: https://open-research.gemmadanks.com/literature/search-for-interstellar-communications/
[project-cyclops-notes-part-i]: https://open-research.gemmadanks.com/literature/project-cyclops-part-i
[technosignatures-literature]: https://open-research.gemmadanks.com/literature/technosignatures-literature-roundup/

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>