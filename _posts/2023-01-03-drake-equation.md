---
title: "The Drake equation"
date: 2023-01-03 T15:20:00
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

Following the first formal proposal in 1959 by Cocconi and Morrison {% cite  Cocconi1959  %}
that humanity was capable of detecting interstellar communications from other intelligent beings in the galaxy and the world's first experiment to attempt to do so (Frank Drake's Project Ozma at the National Radio Astronomy Observatory (NRAO) {% cite  drakeProjectOzma1961  %}), the Space Science Board (1958-1974) of the US National Academy of Sciences and the NRAO agreed to convene a scientific meeting of a small selected group of scientists to "discuss the scientific aspects of establishing radio contact with other planetary systems". This was the first SETI meeting and it happened in November 1961. There are some interesting [historical documents on it in the NRAO archives][nrao-archives-seti]. In preparation for the meeting, [Frank Drake][frank-drake] identified and organised all the parameters required to estimate the number of communicative intelligent civilisations in our galaxy into what is now the famous [Drake equation][drake-equation].

According to the Penn State graduate SETI course materials, the correct reference for the Drake equation is a chapter of [a book called "Current Aspects of Exobiology"][current-aspects-exobiology] published in January 1965, four years after the meeting. The book was based on a symposium called "Current Research in Exobiology" held at the Jet Propulsion Laboratory, Pasadena in 1963. 

Here are my notes from reading this chapter, written by Frank Drake on "The Radio Search for Intelligent Extraterrestrial Life" {% cite  drakeRADIOSEARCHINTELLIGENT1965  %}.

I am tracking all of the papers I've read and want to read on this topic in this [roundup of the technosignatures literature][technosignatures-literature].

## Intelligent extraterrestrial life is inevitable
This book chapter was published right at the emergence of the SETI field. There had been a flurry of papers {% cite  bracewellCommunicationsSuperiorGalactic1960  Cocconi1959  drakeProjectOzma1961  dysonSearchArtificialStellar1960  kardashevTransmissionInformationExtraterrestrial1964  schwartzInterstellarInterplanetaryCommunication1961  %} (you can read my notes on these [here][cocconi-morrison-1959-notes], [here][bracewell-1960-notes], [here][schwartz-townes-1961-notes], [here][drake-1961-notes], [here][dyson-1960-notes] and [here][kardashev-1964-notes]) and a couple of scientific meetings on the topic.

Drake starts the chapter by emphasising the importance of the search for extraterrestrial life and the profound impact it will have once found. Their existance is "virtually inevitable", given the number of sun-like stars in our galaxy. But he also points out that the search space is enormous and costly to cover and that our knowledge (at the time) not good enough. So we must first identify the best strategy that will lead to success at minimum cost. 

## The Drake equation

Estimating the distribution of extraterrestrial civilisations leads to an estimate of the most likely distance we need to search, which informs our choice of search method. 

Drake proposed his famous equation to stimulate discussion on the different factors that contribute to how many extraterrestrial civilisations in our galaxy possess technology advanced enough that they are detectable over interstellar distances (he calls these "communicative civilisations"). A consensus on estimated values of each parameter in his equation was reached at the first SETI meeting. The number, $$N$$, of communicative civilisations in our galaxy is equal to:

$$ N = R_* f_p n_e f_l f_i f_c L $$

Where:
- $$R_*$$ = mean rate of star formation 
  - This was the only parameter thought to be well established at the time at around one per year: now thought to be around 3 solar masses per year
- $$f_p$$ = fraction of stars with planets
  - Unknown at the time but estimated at 0.5: now thought to be closer to 1
- $$n_e$$ = mean number of habitable planets in each planetary system
  - Drake estimated this to be 2-3 and according to a recent study there is likely to be a maximum of 7 {% cite  kaneDynamicalPackingHabitable2020  %}
- $$f_l$$ = fraction of habitable planets on which life evolves
  - The consensus at the time was that the evolution of life on a habitable planet is inevitable and so Drake estimated this as 1
- $$f_i$$ = fraction of the inhabited planets on which intelligence evolves
  - This is completely unknown but Drake suggested that intelligence is an inevitable product of evolution and estimated a value close to 1
- $$f_c$$ = fraction of planets with intelligent life where technology has reached a level sufficient for detection over interstellar distances
  - Conceeding that not all intelligent life develops technology (dolphins were of interest at the time and one of the attendees at the first SETI meeting was [John Lilly][john-lilly], a researcher in dolphin communication. The group of scientists at that meeting called themselves The Order of the Dolphin) this fraction was introduced, although Drake argued it is, nevertheless, close to 1 since multiple intelligent species can evolve and one is likely to develop technology
- $$L$$ = mean lifetime of a communicative civilisation, which is unknown.

The original values estimated for each parameter lead to $$N$$ being equal to the mean longevity, $$L$$, which is completely unknown. Humanity has only been communicative for 100 years and whether or not we survive and/or remain communicative much longer depends on whether we put our technology to good use or mis-use. This is something we are currently struggling with (pandemics, nuclear war, biodiversity loss and climate change being just a few of the risks our immature civilisation faces), but another civilisation might be better at it. 

Drake put a "conservative" estimate on the longevity of a communicative civilisation on the order of 1000-10,000 years and estimated one in $$10^7$$ stars in our neighbourhood hosts a planet with another communicative species, with a mean distance between them of 1000 light years. 

## Modes of communication
Drake listed three possible means of communication that are known to us and evaluates the merits of each. He based his conclusions largely on the economy of each, which he proposed is something that will direct the decisions of any civilisation. 

### Transport of material across space
Spacecraft and probes must travel at velocities much lower than the speed of light and therefore would just take too long for efficient communication, although Bracewell argued that probes could be an efficient means of connecting many stars into a network {% cite  bracewellCommunicationsSuperiorGalactic1960  %} and that we should search for these artifacts in our own solar system. Transporting material through space is also much more costly than other means of communication and so Drake argued it would be rare.

### Radiation of nuclear particles
Drake was quick to rule this out since nuclear particles would cost so much more to produce than electromagnetic radiation and would contain the same information.

### Electromagnetic radiation
The cheapest and easiest mode of interstellar communication is via electromagnetic radiation. This, however, gives an enormous search space since the best sensitivity and range come from narrowband signals which give around $$10^{10}$$ possible frequency bands to search. Drake concluded that more needs to be known about what frequencies are most likely before we can invest a large amount of resources into conducting searches. 

#### What frequency?
The lower the frequency the cheaper a signal is to send since the energy requirements are lower. Background radiation, however, increases as frequency decreases. So there is a minimum frequency for best sensitivity that Drake argued might be most often used for interstellar communication. 

Drake presented calculations of cosmic noise and received power to show that only cosmic noise controls the frequency of best sensitivity, and that radio frequencies are more likely than optical ones. The optimum frequency, based on observations of cosmic noise, would lie between 3.7 and 9.3 GHz (the range is due to different levels of cosmic noise in different parts of the sky). 

This conclusion was based on the assumption that the product of power, gain and effective collecting area of the receiving antenna is not enhanced by more than a factor of $$10^6$$ for optical frequencies over radio frequencies. Drake thought it would be unlikely for such relative growth in optical capabilities but given the advances in laser technology since the 1960s this may not be true (I will find out more about this when I read more on optical SETI). 

Later in the chapter Drake also considered the interstellar hydrogen line, which had been proposed by Cocconi & Morrison {% cite  Cocconi1959  %} and used independently by Drake prior to this publication in Project Ozma {% cite  drakeProjectOzma1961  %}. He concluded that a less noisy frequencies would be the [harmonics][harmonic] of the line. 

#### What duration?
Since the product of bandwidth and pulse duration of a transmission is equal to 1 for the same sensitivity, rather than transmitting a narrow-band signal for a long duration, a signal could cover a broad range of frequencies if it was sent in short enough bursts (0.1 nanoseconds to cover the radio window of Earth's atmosphere). Anything in between is also a candidate mode of communication. This means we need to look at different durations of signal as well as different frequencies. 

Two problems occur with short pulses. They may become smeared in time by interstellar electrons and the power required by the transmitter becomes higher as the pulse duration is shortened. So longer pulses are more economical and so Drake argued these would be preferred.

## Detecting unintentional signals
In the last part of the chapter Drake addresses the detection of unintentional radiation by a technological civilisation. This would require aggregating numerous transmissions to detect a signal. Drake suggested using a similar method to what is used in radar and cross-correlating of two scans of a star. The signals will be correlated but the noise will not be. He simulated data to show that this method of "eavesdropping" on another civilisation is possible and advantageous if a large number of frequencies are used - and adds that our transmissions may already have been detected. I plan to search for later studies attempting to use this method. 

## Summary
This chapter gives an overview of the progress made in the early days of SETI. Drake outlined his equation for estimating the number of civilisations galaxy with technology that would be detectable by us. Using best estimates for the parameters of his equation at the time (only one was thought to be known), he put this number at $$10^7$$ in our neighbourhood, with a mean separation of 1000 light years. 

Drake argued that radio signals are the most likely mode of sending intentional communication across interstellar distances and proposed an optimum frequency range of 3.7 and 9.3 GHz, which accounted for cosmic noise and the economy of transmission. Slower transmissions are more economical than short pulses and therefore more likely. 

Drake also proposed using cross-correlation of two scans of a star to detect unintentional radio transmissions by another civilisation. 

He concluded the chapter with a recommendation that a large number of frequencies should be searched and that a 91 m telescope or larger, collecting data for 30 years would give a high probability of success if the estimated number of civilisations in our neighbourhood is correct. 

Drake finished with the advice, based on experience during Project Ozma, that a scientist involved in the search should spend half their time on this work and half on "more conventional research" to avoid loss of motivation at not having a flow of positive results.


## References

{% bibliography --cited %}
[bracewell-1960-notes]: https://open-research.gemmadanks.com/literature/communications-superior-galactic-communities/
[centaurus-a]: https://en.wikipedia.org/wiki/Centaurus_A
[cocconi-morrison-1959-notes]: https://open-research.gemmadanks.com/literature/search-for-interstellar-communications/
[cta-102]: https://en.wikipedia.org/wiki/CTA-102
[current-aspects-exobiology]: https://www.elsevier.com/books/current-aspects-of-exobiology/mamikunian/978-1-4832-0047-7
[drake-1961-notes]: https://open-research.gemmadanks.com/literature/project-ozma/

[drake-equation]: https://en.wikipedia.org/wiki/Drake_equation
[dyson-1960-notes]: https://open-research.gemmadanks.com/literature/dyson-spheres/
[frank-drake]: https://en.wikipedia.org/wiki/Frank_Drake
[harmonic]: https://en.wikipedia.org/wiki/Harmonic
[john-lilly]: https://en.wikipedia.org/wiki/John_C._Lilly
[kardashev-1964-notes]: https://open-research.gemmadanks.com/literature/kardashev-civilisations/
[m87]: https://en.wikipedia.org/wiki/Messier_87
[my-research-process]: https://open-research.gemmadanks.com/planning/my-research-process/
[nikolai-kardashev]: https://en.wikipedia.org/wiki/Nikolai_Kardashev
[nrao-archives-seti]: https://www.nrao.edu/archives/items/show/15837
[schwartz-townes-1961-notes]: https://open-research.gemmadanks.com/literature/origins-of-optical-seti/
[shannon-hartley]: https://en.wikipedia.org/wiki/Shannon%E2%80%93Hartley_theorem
[technosignatures-literature]: https://open-research.gemmadanks.com/literature/technosignatures-literature-roundup/
[why-technosignatures]: https://open-research.gemmadanks.com/planning/my-next-research-topic-technosignatures/
[world-counts-energy-consumption]: https://www.theworldcounts.com/challenges/climate-change/energy/global-energy-consumption

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>