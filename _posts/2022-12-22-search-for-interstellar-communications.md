---
title: "The search for interstellar communications"
date: 2022-12-22 T20:11:00
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
One of the first papers on the search for exoplanet technosignatures was published in [Nature][nature] in 1959 by Cocconi and Morrison {% cite Cocconi1959 %}. The authors assume that there is another intelligence somewhere in our stellar neighbourhood that has observed the Sun, inferred that intelligent life might exist in its system and has sent a message to us. The paper examines how we should look for this message. This began humanity's search for extraterrestrial intelligence (SETI). Here are my notes from reading this paper. 

I also created a [Jupyter notebook][jupyter-cocconi-morrison] to reproduce their results to help me understand the paper and explore some questions I had. 

I am tracking all of the papers I've read and want to read on this topic in this [roundup of the technosignatures literature][technosignatures-literature].

# How would another civilisation contact us?
Cocconi and Morrison review different possible channels of communication across interstellar distances and propose radio waves as the most likely method another civilisation would use to send us a message.

## Radio receivers are easy to build
The authors hypothesise that an alien civilisation will know we are a newly evolved society and will send a message that would be picked up by a simple detector. Our society has known about radio waves since their discovery by [Hertz][hertz] in 1886 and we have had the ability to communicate via radio waves (turning them on and off to produce messages in Morse Code) since [Marconi][marconi] developed an apparatus for doing so in 1895. 

## Radio waves pass through planetary atmospheres
Radio waves with frequencies between 1 MHz (the paper uses the previous unit of cycle per second) and 10 GHz can reach receivers on Earth's surface from space, whereas much higher or lower frequencies are absorbed by our atmosphere. The authors therefore propose this frequency band as the rational choice for communication intended for Earth. 

# Competing with background radiation
Any signal intended for us must also be distinguishable from the background radio emissions of both the host star and the galaxy. Cocconi and Morrison propose that for a star similar to the quiet Sun, 10 light years away, a minimum frequency of 10 GHz ($$10^{10}$$ Hz) would be required to distinguish it from background radiation using a mirror 100 m in diameter (most radio telescopes have larger diameters than this). 

In order to understand where the formulae in their paper come from I tried to derive them and then reproduce their results. I was also interested to see what frequencies would be required for other types of stars. I saw that the minimum frequency from smaller, cooler stars has to be higher for us to detect signals above the galactic background radiation.

You can see the results and code from my investigation in [this Jupyter notebook][jupyter-cocconi-morrison]. I am noting down the question as a candidate for further exploration, depending on what has already been done in more recent studies.

## Neutral hydrogen emission line
The authors propose the [hydrogen line][hydrogen-line] (1420 MHz) as a likely frequency of communication since the importance of this frequency in the Universe quickly becomes apparent to astronomers and therefore detectors will be built to measure it.

## Galactic background
Radio waves are emitted by the Milky Way and will interfere with signals, particularly when looking in the direction of the galactic plane.  The authors therefore propose searching for nearby stars away from the galactic plane. They suggest that it is technically feasible for another civilisation to build a source powerful enough to send a signal if source and receiver mirrors are of diameter 200 m.

## Doppler drift
Planets from which a signal might originate will be spinning on its axis and orbitting its star. These movements will cause a shift in frequency of a signal. Cocconi and Morrison suggest this might be +/- ~ 300 kHz.

# Summary
This paper was what started SETI. It proposes how and where to search for messages from another civilisation. The main recommendations are to search sun-like stars within 15 light years in the direction away from the galactic plane (where there is lower background radiation) around the frequency of the hydrogren emission line. Some things the paper did not address and/or I am still wondering about:

- How minimum frequencies vary with star type. This is particularly important since most stars in our galaxy are smaller and cooler than the sun. I started exploring this in the Jupyter notebook [here][jupyter-cocconi-morrison]. 
- Whether the spectra of all stars have a bulge at lower frequecies that cause them to deviate from an ideal blackbody (this causes a shift in minimum frequency).
- What are the minimum frequencies for all local stars, taking into account their actual spectra, distances and position relative to the galactic plane. How does this relate to the frequencies used in SETI observations? 

The final few sentences of the paper nicely summarise the importance of searching for technosignatures:

> Few will deny the profound importance, practical and philosophical, which the detection of interstellar communications would have. We therefore feel that a discriminating search for signals deserves a considerable effort. The probability of success is difficult to estimate; but if we never search, the chance of success is zero.

# References

{% bibliography --cited %}

[hertz]: https://en.wikipedia.org/wiki/Heinrich_Hertz
[hydrogen-line]: https://en.wikipedia.org/wiki/Hydrogen_line
[jupyter-cocconi-morrison]: https://github.com/gemmadanks/technosignatures/blob/main/radio-seti/interstellar-communications/interstellar-communications.ipynb
[marconi]: https://en.wikipedia.org/wiki/Guglielmo_Marconi
[my-research-process]: https://open-research.gemmadanks.com/planning/my-research-process/
[nature]: https://www.nature.com/
[technosignatures]: https://open-research.gemmadanks.com/notes/technosignatures/
[technosignatures-literature]: https://open-research.gemmadanks.com/literature/technosignatures-literature-roundup/
[why-technosignatures]: https://open-research.gemmadanks.com/planning/my-next-research-topic-technosignatures/

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>