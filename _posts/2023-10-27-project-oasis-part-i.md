---
title: "Project Oasis: Part I"
date: 2023-10-27 T20:29:00
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

Project Oasis was the second SETI-related Summer Faculty Fellowship Study in Engineering System Design funded by NASA in cooperation with the [American Society for Engineering Education (ASEE)][asee] and was conducted at the University of Santa Clara and the [NASA Ames Research Center][nasa-ames] in 1979, eight years after Project Cyclops in 1971 (I have notes on the Project Cyclops report {% cite ProjectCyclopsDesign1972 %} in two previous posts: [part i][project-cyclops-notes-part-i] and [part ii][project-cyclops-notes-part-ii]). 

The primary focus of this second project was on the design of a signal detection system for SETI and its name was inspired by the region of the radiomagnetic spectrum thought to be a prime target for finding signals from extraterrestrial intelligence: the "water hole" (proposed in the Project Cyclops report {% cite ProjectCyclopsDesign1972 %} and later [expanded on in a paper][oliver-1979-notes] {% cite  oliverRationaleWaterHole1979  %} by one of its co-directors, Bernard Oliver). 

> Oasis, a patch of green in a vast expanse of arid desert, with its water hole providing the source of life.

Project Oasis involved a group of 22 people who were tasked with solving the following two problems:

- How to process 1/2-terabits ($$10^{12}$$ bits) of data in 1000 seconds (about 16 minutes)
- How to detect a completely unspecified signal with acceptable sensitivity

The group wrote a report {% cite lordProjectOASISDesign1981 %} detailing the design of a signal detection system to meet the needs of the SETI field at the time. This was published in 1981 and was digitised by NASA in 2013 -- it is publicly available online:

[Project Oaisis: The Design of a Signal Detector for the Search for Extraterrestrial Intelligence][project-oasis-1981-report]

Since the Project Oasis report is 443 pages long, I am splitting my notes into multiple posts. Here are my notes from reading chapter one (of seven), which gives a nice overview of the state of the SETI field at the time and an outline of the proposed signal detection system. 

You can find my notes on other classic SETI papers in my [roundup of the technosignatures literature][technosignatures-literature].

## Progress in the SETI field
The introduction to the report highlights the progress and discoveries made in the previous decades that enables the search for extraterrestrial intelligence (SETI) to move from science fiction to science fact:

- The organic molecules necessary for life (on Earth) are found all over the universe.
- The Sun and Earth are average members of the galaxy: there is nothing unique about them.
- Technology has advanced enough that we are capable of interstellar communication.

## Current state of the SETI field
The rest of the first chapter summarises background information on the field, including the consensus at the time on:
- Where to look
- How to look
- Why look
- How to understand a signal
- The current status of the search

The authors also provide an outline for the design of the Oasis Signal Detection System, which would be able to find and recognise a signal emitted by extraterrestrial intelligence (ETI) using multi-channel spectrum analyzers (MCSAs).

### Where to look
The most likely places to find life, and therefore the best candidate stars to search, are around parent stars that are:
- Not too large (or it would burn out too quickly for intelligent life to evolve).
- Not too small (or a planet must be so close to the star to have enough heat to be habitable that it would become tidally locked, causing the atmosphere on the dark side of the planet to freeze).
- Rotating slowly, which indicates most of the initial angular momentum (98% in the case of our solar system) has been lost to a planetary system.
- Second generation or later since the heavier elements needed for life are only found in the exploded debris of stars.
- Single star systems, since the planets of multi star systems are less likely to have stable orbits.

There are around 20 million such stars in our galaxy.

### How to look

#### Radio signals
Signals using electromagnetic radiation are the most cost-effective (in time and energy) means of communication across interstellar distances. In the 70s the most popular view was that the radio region of the spectrum was the best place to search. Optical signals were seen to have two major short-comings in that they are likely to be:

1. Outshone by the parent star
2. Absorbed by interstellar dust

Radio signals do not have these problems and the technology of the late 70s was already capable of transmitting and receiving radio signals over distances of 100,000 light years.

#### Anticryptography

Transmissions from ETI can be grouped into two categories and the Oasis signal detection system is designed to find both:
1. Internal transmissions that leak out into space (like our TV and radio broadcasts). These are weaker and harder to find.
2. Beacons that are intended for attracting the attention of other civilisations, which are likely to be optmised for easier detection.

If a signal is designed to be as easy as possible to decipher (anticryptography), then if a dimension of the search space can be reduced it will be. An optimal signal will therefore be:
  - Omni-directional
  - Transmitted continuously
  - Circularly polarised
  - Narrow band
  - Doppler corrected

We can use this to focus the search.

### Why look
We are more likely to detect signals from more advanced civilisations than our own (less advanced civilisations are not yet able to communicate and the chance of finding a civilisation at the same stage of development as us is small). 

If we found another civilisation, therefore, we would benefit from the following:
- We'd have evidence that not all civilisations destroy themselves before reaching maturity. 
  - This might inspire us to work harder on reducing our own existential risks.
  - We may gain knowledge to help us achieve this goal ourselves.
- It would change our perspetive on the smaller problems we have. 
- New frontiers and challenges will prevent "cultural stagnation" of our civilisation. 

### How to understand messsages
An initial message is likely to be built around the common knowledge or experiences of all civilisations in the galaxy in order to have the best possible chance of being understood. Numbers and counting would be one example. The report refers to Lingua Cosmica ([Lincos][lincos]) to show that this is possible. Lincos, a language created by Hans Freudenthal in the 60s, uses messages with a counting sequence to define numbers and then introduces one new mathematical symbol at a time, which are then used to build more complex messages as a means of establishing communication with another civilisation.

### The status of the search
Several studies and small scale searches had been conducted, using existing telescopes, from 1960 to 1979 (the [first, Project Ozma, by Drake][drake-1961-notes] looked at two stars for two weeks as a proof of concept). Most spent a few days or weeks searching. The longest was an ongoing 6 year all sky survey. Most observatories at the time did not look for extraterrestrial signals at all. The authors of the Oasis report likened this effort (compared to what was possible) to conducting a survey for earthquakes in California by standing outside for 10 minutes and noting any vibrations.

Previous SETI projects searched for two types of signals:
- Wideband pulsed signals (very few projects):
  - Widely separated receivers (thousands of km) with non-directional antennas used to record pulsed signals that are cross correlated to remove interference. Any signal that remains is likely to be of extraterrestrial origin.
  - Pulsar detection equipment were also being used to detect wideband pulses.
- Narrowband continuous signals from specific targets (most projects)
  - Banks of analog filters for moderate bandwidth (10 kHz) and number of channels (50)
  - Autocorrelation receivers for more channels (1000) that digitally compute the [Fourier Transform][fourier-transform] of the autocorrelation function of the incoming signal (either in real-time or later using computers or a laser and lens system)
  - The resulting power spectrum of the signal is then inspected for peaks

The all sky survey in Ohio, which was ongoing at the time of Project Oasis, used the following strategy:
- Ignore signals from large astronomical objects and short-time peaks by cross-correlating with the antenna pattern
- Ignore that occur in more than one channel (i.e. wide-band signals)
- Use a narrowband filter to re-examine any remaining signals at higher resolution
- Ignore signals that are present in two different beams (beam-switching) to remove interference from radio sources on Earth  

Several other studies had re-examined data collected for different purposes or used "parasitic" receivers on telescopes to examine signals from wherever the telescope happened to be looking.

### The next step
The authors of the report argue that further advances in the search require receiving equipment designed and constructed specifically for SETI. These new receivers can be used with existing radio telescope antennas. 

In order to design such receivers we need to:

- Determine what type of signals to expect
  - Beacons as well as unpredictable signals (e.g. from leakage)
- Design optimum search algorithms to detect them
- Plan for a full-time, long-term search at several observatories
  
Since there is increasing radio interference, particularly from artificial satellites, that will eventually make the search impossible without moving into space or the moon it is urgent to start now.

### The receiving system
The system designed as part of Project Oasis consists of:
- A radio telescope examining a target star for up to 1000 seconds
  - Two orthogonally polarised feed anntenas
  - Two separate receivers
  - Two separate Multi-Channel Spectrum Analyzers (MCSAs)
    - A device specially designed for SETI purposes that can analyse 8 MHz of bandwidth at 1 Hz resolution
      - The 8 MHz band is split into 120 bands using a digital bandpass filter bank
      - Each band is subdivided into 1 Hz bands by 120 microprocessors that compute the Discrete Fourier Transform of the filter outputs
      - Output data rate will be 16 Mb per second, requiring a total of 16 Gb of data storage
- The Oasis Signal Detector that searches the final output for possible intelligence

### The purpose of Project Oasis
The purpose of the study was to begin the next step in the search for extraterrestrial intelligence: design the part of a specialised SETI receiver that finds and recognises a signal. The authors were confident that the system would eventually be constructed after some refinement.

### The Oasis Signal Detection System
The Oasis system embodied three separate signal detection philosophies for seeking different types of signals:
1. Carrier Wave Signal Detector
  - Near zero bandwidth, may be drifting slowly with time (extreme case)
2. Pulse Signal Detector
  - Broad bandwidth, may be pulsed in time (other extreme case)
3. Battery of Tests
  - All signals in between the extreme cases (unpredictable cases). These include:
    - Complex Coherence
    - Polarization
    - GCV by Row
    - ANOVA Row
    - ANOVA Column
    - ANOVA Interaction
    - Total Power
    - Goodness of Fit
    - Narrowband Pulse

## Summary
Following on from Project Cyclops eight years earlier, Project Oasis focussed on the design of a signal detection system that would find both intentional (beacons) and unintentional (leakage) signals from extraterrestrial civilisations. The first chapter of the 443-page long technical report from this project summarises the state of the SETI field as of 1979 and outlines the design of the Oasis signal detector. The authors were confident that the search was both feasible and urgent. 

The following chapters provide further details and I will document my notes on these in separate posts. Chapter two covers the characteristics of signals and noise and how to differentiate between them, which is the main task of the Oasis signal detector.

## References

{% bibliography --cited %}

[asee]: https://www.asee.org/
[drake-1961-notes]: https://open-research.gemmadanks.com/literature/project-ozma/
[fourier-transform]: https://en.wikipedia.org/wiki/Fourier_transform
[lincos]: https://en.wikipedia.org/wiki/Lincos_language
[nasa-ames]: https://www.nasa.gov/ames
[oliver-1979-notes]: https://open-research.gemmadanks.com/literature/water-hole-rationale/
[project-cyclops-notes-part-i]: https://open-research.gemmadanks.com/literature/project-cyclops-part-i/
[project-cyclops-notes-part-ii]: https://open-research.gemmadanks.com/literature/project-cyclops-part-ii/
[project-oasis-1981-report]: https://ntrs.nasa.gov/citations/19820016111
[technosignatures-literature]: https://open-research.gemmadanks.com/literature/technosignatures-literature-roundup/

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
