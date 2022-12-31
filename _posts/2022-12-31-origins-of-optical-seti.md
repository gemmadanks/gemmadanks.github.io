---
title: "Interstellar communications by optical masers"
date: 2022-12-31 T13:32:00
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

In 1961, a paper published in Nature by [Schwartz and Townes][schwartz-townes-1961] {% cite  schwartzInterstellarInterplanetaryCommunication1961  %} was the first to propose that extraterrestrial intelligence may use an optical beam for communication with Earth. This was in response to earlier papers that proposed searching for [communications in the radio range of frequencies][cocconi-morrison-1959-notes] {% cite  bracewellCommunicationsSuperiorGalactic1960  Cocconi1959  %}. Here are my notes on this classic paper.

I am tracking all of the papers I've read and want to read on this topic in this [roundup of the technosignatures literature][technosignatures-literature].

# Optical Masers
At the time this paper was written [Charles Townes][charles-townes] (one of the authors), was working on the development of the [maser (microwave amplification by stimulated emission of radiation)][maser] and the optical maser, which was ultimately named the [laser (light amplification by stimulated emission of radiation)][laser]. Three years later Townes shared the [1964 Nobel Prize for Physics][nobel-prize-physics-1964] for his work. 

In this paper, the authors state that maser techniques were still in a "rudimentary stage" but that it was only a "historical accident" that they weren't discovered before radio. It is possible, therefore, that an extraterrestrial intelligence would choose to send messages via optical signals. Optical lasers today are much more efficient than radio transmitters.

## Transmitting optical signals from an exoplanet
Schwartz and Townes considered two different optical lasers that might send interstellar signals to us:
- A single 10 kW beam at 500 nm (5000 $$\unicode{x212B}$$) with a 1 MHz bandwidth and a 5 m diameter reflector (the largest telescope at the time). This beam would be effective above a planetary atmosphere and would be visible by the naked eye from 0.1 light years away.
- A collection of 25 of the above lasers to give an effective aperture of 10 cm, which would be more suitable for a ground-based transmitter given atmospheric turbulence. This would produce an intensity of radiation 100 times lower than the single laser and would be visible with the naked eye at a tenth of the distance.

## Detecting optical signals on Earth
Schwartz and Townes take the suggestion by Cocconi and Morrison {% cite  Cocconi1959  %} that we should search stars within 10 light years from Earth. At this distance an optical signal sent using the single laser would be seen visually with the largest telescope at the time (the 5 m [Hale telescope][hale-telescope]; today's [largest optical telescopes][largest-telescopes] have diameters more than double this) and the group of 25 lasers would require 1.5 hours exposure.

### Resolving signals against background radiation
Schwartz and Townes proposed that it would be easier to discriminate between an optical beam sent for communication and stellar radiation by using high resolution spectroscopy. Using the Sun as a representative star, the single laser beam would have an intensity 25 times that of the Sun but the collection of lasers would produce 1/4 of the intensity. 

The authors proposed using frequencies of transmission that are either in the far violet or that fall in the range of prominant absorption lines (e.g. Ca II, H or K) for the host star (which would produce 300 times the intensity of the radiation from the host star using the single laser). The beams from the single laser transmitter could be resolved by the leading spectrometers of the time but the beams from the 25 lasers would not be (higher resolution is possible today).

### Accounting for changes in Doppler shifts
Since Earth and the exoplanet are rotating about their own axes and their stars, the Doppler shift in any signal sent from them would change over time. Unless already accounted for by the transmitter, this shift might be greater than the resolution of the spectrometer and so exposure times would have to be limited to one hour, which would allow detection from stars 10 light years away. 

## Summary
Schwartz and Townes proposed examining high-resolution stellar spectra for lines that are unusually narrow, with unusual frequencies for the star type and are varying in intensity in order to detect possible candidates for optical interstellar communications from extraterrestrial intelligence. Their paper set out a strategy that was within or just beyond the capabilities of technology in the early 1960s. This restricted the search to stars within 10 ly away. Today we have more advanced telescopes and higher resolution spectrometers and can search more of the sky.

Since the publication of this landmark paper there have been several attempts to search for optical signals. This has become known as optical SETI (OSETI) and I will be reading more about it in later papers.

## References

{% bibliography --cited %}

[charles-townes]: https://en.wikipedia.org/wiki/Charles_H._Townes
[cocconi-morrison-1959-notes]: https://open-research.gemmadanks.com/literature/search-for-interstellar-communications/
[hale-telescope]: https://sites.astro.caltech.edu/palomar/about/telescopes/hale.html
[largest-telescopes]: https://en.wikipedia.org/wiki/List_of_largest_optical_reflecting_telescopes
[laser]: https://en.wikipedia.org/wiki/Laser
[maser]: https://en.wikipedia.org/wiki/Maser
[my-research-process]: https://open-research.gemmadanks.com/planning/my-research-process/
[nature]: https://www.nature.com/
[nobel-prize-physics-1964]: https://www.nobelprize.org/prizes/physics/1964/summary/
[schwartz-townes-1961]: https://www.nature.com/articles/190205a0
[technosignatures-literature]: https://open-research.gemmadanks.com/literature/technosignatures-literature-roundup/
[why-technosignatures]: https://open-research.gemmadanks.com/planning/my-next-research-topic-technosignatures/

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>