---
title: "Project Cyclops - Part II"
date: 2023-05-18 T10:21:00
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
This is my second post on Project Cyclops, a NASA study from 1971 that proposed a system for detecting extraterrestrial intelligence. These are my notes from reading the second part of the original report, which presents details of the Cyclops system together with cost estimates, conclusions and recommendations. The first part of the report contains introductory material about the search and you can read my notes on this here:

[Project Cyclops - Part I][project-cyclops-1972-notes-i]

The entire report was digitised by NASA in 2013 and is publicly available online:

[Project Cyclops: a Design Study of a System for Detecting Extraterrestrial Intelligent Life][project-cyclops-1972-report]

While the authors of the report declared the study as "extremely preliminary" and "a rough set of estimates", it became known as "The Bible of SETI" and influenced SETI research for decades, in particular by reaffirming that radio wavelengths should be prioritised.

You can find my notes on other classic SETI papers in my [roundup of the technosignatures literature][technosignatures-literature].

## The Cyclops System
Chapter 7 of the report summarises the following four chapters, which go into the technical details of the Cyclops system design. The system itself could be used for many different purposes. It is the signal processing that is unique to detecting extraterrestrial intelligence.

### Phased arrays
A microwave antenna system with a collecting area of 7-20 km$$^2$$ (3-5 km aperture diameter) is required to detect extraterrestrial signals. This must be constructed as a ground-based phased array of smaller antennae due to the cost and practicalities involved in a telescope of this size and the uncertainty in the required collecting area. A phased array can be expanded over time as required. 

The authors estimated that the cost of constructing these arrays scales as the square of the diameter and therefore recommended that each array is made as large as possible (i.e. 100 m in diameter). They also evaluated various mounts and recommended using a conventional mount with azimuth and elevation axes.

To avoid shadowing one another the arrays must be separated by three times their diameter. The optimal layout of antennae would be roughly circular in a regular hexagonal lattice. A control and data processing centre would be best positioned at the centre of the circle:

>From the air, the final Cyclops system would be seen as a large central headquarters building surrounded by an "orchard" of antennas 10 km to 10 miles in diameter and containing 1000 to perhaps 2500 antennas.

A system of underground service tunnels would allow the transmission of power, control signals and radio signals from the antennae to and from the central building. They would also allow airflow and contain telephone cables.

The authors also briefly discuss the options for creating a community ("Cyclopolis") for staff and their families, either a few miles away or between the antennae:

> There would be ample room between the antenna elements for playgrounds and recreation facilities.

The main problem would be radio interference, but they did not study this.


### Sky coverage
The probability of contact with an extraterrestrial intelligence is proportional to the fraction of sky we search. With one telescope, sky coverage is higher the closer to the equator it is positioned:

> If only one Cyclops system is ever built, a nearly equatorial or slightly southern latitude is technically (though perhaps not politically) preferable.

Complete sky coverage would be possible with two or more systems positioned north and south of the equator.

Other features of the site for the Cyclops system ideally include:

- Low geological activity (no earthquakes or subsidence)
- High dry plateaus (to avoid atmospheric turbulence from humidity and clouds)
- Mild climate (no snow or high winds that deform the antennae)
- A large plane area (to simplify processing and phasing)
- Remote (to avoid radio intereference from civilisations on Earth)
  
### Receiver system
A receiver system covering the frequency range from 0.5 to 3 GHz would be best for the microwave window that the study concluded is most likely to contain extraterrestrial signals. 

Heterodyne receivers at each antenna would convert the radio frequency to a fixed band for transmission. 

Low noise is essential (halving the noise is equivalent to doubling the antenna area and the authors estimate that the Cyclops system can achieve a noise as low as 20 K) and remote tunability is required with so many antennae to coordinate. 

An instantaneous bandwidth of 100 GHz is possible with this system for two polarisations simultaneouosly and the authors suggest covering the entire 'water hole' may be possible if the bandwidth is increased through further study. 

### Signal processing
The authors assume that any extraterrestrial signal will be characterised by:

> ...very narrow, needlelike peaks in the power spectrum that may drift slowly with time but can be seen if we can resolve the power spectrum sufficiently and follow the drift.

After subdividing the signal into bands of 1-10 MHz, signal processing to find these needle-like signals consists of the following steps:

1. Transform the received signal into a power spectrum (amplitude vs. time to energy vs. frequency)
2. Add the power spectra at different offsets of adjacent samples to account for drift
3. Detect spikes above noise in the added spectra 

Each star observed across 200 MHz for 1000s would give 100 samples of its power spectrum at 0.1 Hz resolution. Added in 400 different ways to account for different drift rates would result in $$4 \times 10^{11}$$ tests.

An optical spectrum analyzer was suggested for data processing since digitising the signal and applying a fast Fourier transform would be too costly.

Analog data storage was the technology of the time, although the authors suggested that magnetic [bubble memory][bubble-memory] could be an ideal digital alternative once the costs were lower (this type of memory was used in the 1970s and 1980s but was replaced by semiconductor memory, which is much faster).

### Signal detection
The authors computed and plotted the signal to noise ratio for different probabilities of missing a signal, when requiring a false alarm probability of $$10^{-12}$$ and concluded that with 100 samples and a resolution of 100 MHz, a signal that is 90 dB below the noise threshold could be detected. This is the size of the needle that Cyclops would be able to find in the millions of haystacks it would examine.

### Range 
The Cyclops system would detect a 1000 MW beacon at 1 Hz resolution and observing time of 1000 seconds at a range of 100 light years per km of clear aperture diameter (about one third of the physical diameter of the antenna due to spacing).

### Detecting other types of signal
The Cyclops system was designed to detect narrow-band signals that do not change much over time or frequency. They are assumed to be a type of beacon. But the authors also proposed a way to detect broader bandwidth signals or pulses using an optical analyzer, scanning the power spectrum or photographing it to look for anomalies.

[Drake previously proposed][drake-1965-notes] cross-correlating two power spectra taken at different times to detect weaker signals. The authors of the Cyclops report suggested using this method in addition to the proposed signal analysis to maximise the results. Terrestrial interference would have to be removed for this to work. 


### Terrestrial interference
Radio signals from Earth pose a problem for the Cyclops system since it will scan the same radio frequency bands. If known frequencies from terrestrial sources are ignored it would create blind spots for Cyclops. Some interference can also be removed by using a larger concentric secondary beam that can be subtracted from the primary beam. Alternatively, a "quiet" zone around Cyclops could be created. Radio interference from Earth continues to be a problem in SETI today.


### Cost
There is a very nice figure (Fig. 7-3) showing the cost (and time) estimated at the time as a function of clear aperture diameter.

> A rough guess of $100 million is shown for engineering costs. Building costs are shown at $10 million and the companion optical system at $2 million. Road and utility costs are highly site dependent and have not been included.

With an ultimate size of 5 km the authors estimated a total structures cost of 10-25 billion dollars.

The authors estimated that the primary narrow band coherent signal detection system would cost $125 million to $500 million, with cost being proportional to the bandwidth and observing time. They also emphasised that technology for data processing is advancing rapidly and that their cost estimates and suggested system may be quickly outdated.

### Comparison to Project Ozma

Compared to an earlier attempt to detect signals from extraterrestrial intelligence from two nearby stars ([Project Ozma][drake-1961-notes]), the Cyclops system would search two million times as broad a band and would detect signals at 2000 times the distance at the power required for detection by Ozma.  

> The T-Cetacians or e-Eridanians would have to have been irradiating us with an effective power of about 10$$^{13}$$ W to have caused a noticeable wiggle of the pens of Ozma's recorders; 2.5 MW would be detected by Cyclops.

## Cyclops as a beacon
In Chapter 12, the authors of the report discuss using Cyclops as a beacon. This could be beneficial if, for example, we search the nearest 1000 stars with no signal detected then send a beacon to these stars, wait a while for a response and scan them again. 

Two different beacon systems were considered:
- Sending a high powered beacon to a single star using the entire Cyclops array (with a range of 50 light years for a receiver with no reflector; 80 light years for a 10 m receiving antenna; and 800 light years for a 100 m receiving antenna)
- Sending weaker beacons to 1000 different stars using the array elements individually (the range is then reduced by a factor of 1000). 

The authors concluded that the latter approach would involve data processing that would be too expensive but that the former is worth doing:

> We conclude that Cyclops can, and probably should, be used as a beacon to illuminate stars closer than 100 light-years, during certain portions of the search phase.

## Search strategy
The Cyclops system is limited to searching a single star at a time. In order to minimise the time spent searching, stars should be targetted in order of highest probability that they are transmitting a detectable signal. This probability is a function of the distance to the star (signals from closer stars will be easier to detect) and its spectral type (which affects the probability that technologically advanced life has evolved there).

A contour plot of how the probability varies with distance and spectral type gives a "mountain" with a peak that can be explored first before descending to lower altitudes:

> It is like examining the emerging shoreline of an island in a subsiding sea. 

At the time the report was written, the distances were only known for a few hundred target stars and the authors highlighted that developing a comprehinsive list of stars is the first step yet to be taken. A lot of work has been done on measuring the spectra and distances to stars since the 1970s (the [Gaia project][gaia-dr3] has published distances of over 1 billion stars in the Milky Way). 

The authors proposed additional studies on habitability of planets and what stars are the most likely candidates to target search efforts. They assumed that F type stars were the hottest main sequence stars that could support planets with life (given the time taken to evolve life on Earth) and that K1 or K2 stars would be the coolest (since tidal locking would become a problem). But the range of spectral types could be much narrower (or broader) and the number of targets could expand enormously if lower temperature stars could support life since these form the majority of all stars.

Additional benefits of the Cyclops system would be the ability to study the corona of other stars as well as their planetary architectures.

The authors envisioned four phases of the search:

1. Preoperational phase: planning the build and generating a list of target stars
2. Construction years: 100 antenna per year for 10-25 years, searching the nearest target stars with the first few antennae: 15,000 stars per year; 2000 seconds per star. Half the time devoted to leakage scans and radio astronomy and the other half to searching for beacons.
3. Total complete search out to 1000 light years plus transmitting beacons.
4. Long-term effort if no signals are found and consideration of building a long-range beacon.

They also recommended searching the galactic centre for possible beacons from an existing network of extraterrestrial intelligences.

## Cyclops for other research
In chapter 14, the authors put forward several areas of research that would benefit from the development of the Cyclops System. These included: deep space exploration, radar observations of planets in the solar system; extra-galactic radio sources; pulsars; stellar coronas; technology for radio astronomy.

## Conclusions and recommendations
The final chapter of the Cyclops report lists conclusions, recommendations and premises that these were built on. These were presented as the consensus of the group with the caveat that some may not completely agree with individual points.

### Premises
- Planetary systems are the rule, not the exception (now known to be true)
- Many planetary systems will contain at least one planet in the habitable zone (called "stellar ecosphere" in the report)
- Organic precursors of life are abundant
- Main sequence stars cooler than F5 stars have long enough life times for the evolution of life
- Planets around main sequence stars cooler than K7 (or K5) are likely to suffer from tidal locking and are unlikely to host life
- A substantial fraction of stars will have habitable planets that will at some point host intelligent life
- The longevity of a communicative civilisation is completely unknown and can only be estimated once contact with one has been established
- The lifetime of a civilisation may be prolonged as a result of interstellar contact due to the knowledge they may share

### Conclusions
Given the premises above, the authors of the Cyclops report concluded:

- Present knowledge of the laws of physics indicates that communication via signals is much more economical than other ways of establishing contact (e.g. probes and spacecraft)
- An expandable search system is best given the uncertainty in the search range
- Microwaves are the best means of communication since the energy requirements, costs and technical requirements are lower than for other wavelengths
- The best frequency is 1 - 3 GHz, due to the costs, lower Doppler rates and the stability of the signal
- The quiet frequency window between the spectral lines of hydrogen and the hydroxyl radical (the "water hole", 1420 - 1662 MHz) may be an enticing region of communication for water-based lifeforms
- The Cyclops system could, in theory, be expanded to 100 or more square km
- Microwave communication is possible across intergalactic distances with antenna sizes of a few km and high-speed interstellar communication would allow rapid transmission of information
- Both low powered directed beamed signals and high powered omnidirectional beacons are possible
- Beacons will be circularly polarized, highly monochromatic (spectral widths of 1 Hz or less), convey information slowly and include how to respond
- The proposed Cyclops data processing method would permit searching a 100 MHz band at 0.1 Hz resolution, which could be widened to 200 MHz to cover the water hole simultaneously
- Cyclops would cost 6 - 10 billion dollars (in 1970s money), spent over 10 - 15 years, mostly for the antenna structures
- The search may take decades or centuries and requires automation and longterm funding commitment. Faith that it will be worth it is key.
- The search for extraterrestrial intelligent life should be included as part of a "comprehensive and balanced space program"
- More work on the problem and optimum system design should be done (and funded) before the search begins
- Since the search is important for all of humanity, international cooperation should be encouraged by complete dissemination of all information. Building more than one Cyclops system would allow complete sky coverage and continuous reception of received signals.

### Recommendations
The recommendations of the authors included: establishing SETI as a part of NASA's space program; forming an advisory committee; building up competance in system design and techniques for communication with extraterrestrial intelligences; ensuring funding for the project is longterm, should it go ahead; cooperating with international groups; promoting the Cyclops system as a tool for other space projects for part of the time; generating public interest; and making all information publicly available. They also recommended protecting the "water hole" by limiting 1.4 - 1.7 GHz to interstellar communication. 

## Supercivilisations and longevity
The Cyclops project report contains several appendices with further supporting arguments, data, models and mathematics.

Appendix B contains an account of alternative views on interstellar communication and why they are not the basis for the Cyclops system design. These include:

- [Kardashev's classification of civilisation][kardashev-1964-notes] types
  - We have not detected any evidence of type II (that have the energy of their parent star at their disposal) or type III civilisations (energy equivalent to an entire galaxy), despite not needing a system like Cyclops to receive them, so these remain hypothetical
- [Dyson spheres][dyson-1960-notes]
  - The authors of the Cyclops report were sceptical of the possibility of Dyson speheres or swarms (artificial constructs around a star that capture most of its energy) and suggested that any excess infrared radiation produced by them would be indistinguishable from dust clouds. They also noted
  > "...Dyson appears so convinced of the detectability and inevitability of the kind of astroengineering he describes that he construes our failure to detect any such activities as evidence for the absence of advanced intelligent life!" 
- Abiological civilisations
  - In the 1970s artificial intelligence was mainly restricted to the realm of science fiction and early research in the area was about to enter a period of dormancy. The authors of the Cyclops report saw any evolution of artificial civilisations as an extension of their biological precursors, making the distinction between beacons from artificial and biological intelligence irrelevant. Interestingly, they stated that:
  > "It seems very unlikely that an advanced natural species would voluntarily abdicate its dominant position to an artificial species." 

  Today, artificial intelligence is developing rapidly and the emergence of an artificial general intelligence is considered a possible existential risk; we may not have a choice in whether or not it replaces us once it emerges and this may have happened to other civilisations.
- Advanced societies that do not use technology
  - The authors of the report addressed the ideas of advanced civilisations that put technology to the side in order to live in peace and harmony. They viewed this as a hindrance to evolution by natural selection and stated that learning how these societies overcame this problem would be valuable.

The authors pointed out that any prediction of what another society may look like must have a low probability, given how human history has played out and how unpredictable our own technology was to our ancestors (the authors themselves were unable to predict the way technology would develop in the 50 years since they wrote this report). 

> Rather than base our hopes on models that represent extreme extrapolations into the future, it would appear far more productive to apply the assumption of mediocrity to our known present capabilities.

If we assume that another civilisation will eventually consider life elsewhere in the universe and develop a means of communication, we should actively search for them rather than wait for them to send us a signal we cannot ignore.   

They added:

> We must not only weigh the cost of action against the possible benefits to be realized, we must also give some thought to the cost of inaction.

## Summary
The Cyclops Project was hugely influential on SETI research that followed it and represented the first large-scale coordinated effort of experts in the field at the time to tackle its central problem: detecting an extraterrestrial signal when we don't know where to look.

The first part of the resulting report gave detailed background information (you can read my notes on this [here][project-cyclops-1972-notes-i]) and the second part of the report detailed the design, requirements and costs of the proposed Cyclops system and presented conclusions and recommendations for next steps. 

The authors emphasised that more studies on the problem were needed (e.g. compiling a list of stars ordered by probability that they may host a planet with intelligent life) and highlighted the benefits of the Cyclops system to other areas of research. 

The report concluded with the recommendation that the search be part of an open international effort and the authors were of the opinion that communication with another civilisation may improve humanity's longevity, estimates of which were pessimistic in the 70s (and are no better today). 

I enjoyed reading this report. It is packed with background information that was very useful for me and it was fascinating to learn the perspecitves of the time from the SETI pioneers. Some of the technology is, of course, outdated now but it was fun to put it into its historical context, although I would need a lot more time to do this properly. I look forward to reading papers written after this report was published and learning how the field has progressed, particularly with regards to radio vs. optical SETI.

## References

{% bibliography --cited %}

[alpha-centauri]: https://en.wikipedia.org/wiki/Alpha_Centauri
[asee]: https://www.asee.org/
[barnards-star]: https://en.wikipedia.org/wiki/Barnard%27s_Star
[bernard-oliver]: https://www.seti.org/bernard-m-oliver-1916-1995
[bracewell-1960-notes]: https://open-research.gemmadanks.com/literature/communications-superior-galactic-communities/
[bubble-memory]: https://en.wikipedia.org/wiki/Bubble_memory
[cocconi-morrison-1959-notes]: https://open-research.gemmadanks.com/literature/search-for-interstellar-communications/
[cosmos]: https://www.imdb.com/title/tt0081846/
[drake-1961-notes]: https://open-research.gemmadanks.com/literature/project-ozma/
[drake-1965-notes]: https://open-research.gemmadanks.com/literature/drake-equation/
[dyson-1960-notes]: https://open-research.gemmadanks.com/literature/dyson-spheres/
[gaia-dr3]: https://www.cosmos.esa.int/web/gaia/early-data-release-3
[habitable-zone]: https://exoplanets.nasa.gov/search-for-life/habitable-zone/
[hoerner-1961-notes]: https://open-research.gemmadanks.com/literature/waiting-times-and-longevity/
[john-billingham]: https://www.seti.org/john-billingham-1930-2013
[kardashev-1964-notes]: https://open-research.gemmadanks.com/literature/kardashev-civilisations/
[nasa-ames]: https://www.nasa.gov/ames
[palebluemarbles-stars-sand]: https://www.palebluemarbles.com/count-the-stars-in-grains-of-sand/
[poisson-distribution-wikipedia]: https://en.wikipedia.org/wiki/Poisson_distribution
[project-cyclops-1972-notes-i]: https://open-research.gemmadanks.com/literature/project-cyclops-part-i/
[project-cyclops-1972-report]: https://ntrs.nasa.gov/citations/19730010095
[technosignatures-literature]: https://open-research.gemmadanks.com/literature/technosignatures-literature-roundup/
[titus-bode]: https://en.wikipedia.org/wiki/Titius%E2%80%93Bode_law


<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>