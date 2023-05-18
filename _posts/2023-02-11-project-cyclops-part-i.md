---
title: "Project Cyclops - Part I"
date: 2023-02-11 T14:41:00
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
The Cyclops study was a 1971 Summer Faulty Fellowship Program in Engineering Systems Design, funded by NASA in cooperation with the [American Society for Engineering Education (ASEE)][asee] and conducted by Stanford University and [NASA Ames Research Center][nasa-ames].

The SETI field was still in its early days and this project represented the largest effort made so far to study the problem. It was co-directed by [Bernard Oliver][bernard-oliver] and [John Billingham][john-billingham], who became leaders of the field, and included faculty members of various universities across the USA. 

Their subject was the design of a system for detecting extraterrestrial intelligent life and their primary objective was to **assess the requirements of mounting a realistic effort in detecting extraterrestrial intelligence (ETI)**. 

It had contributions from several pioneers in the field, including Philip Morrison who was the [first to formally propose a search][cocconi-morrison-1959-notes], Ronald Bracewell who suggested [searching for probes sent out by ETI][bracewell-1960-notes] and Sebastian von Hoerner who proposed [estimates for longevity and distance between extraterrestrial civilisations][hoerner-1961-notes]. 

The conclusions of the Cyclops study, together with introductory material on the topic and a suggested system design with cost estimates, were published in January 1972 in a 253 page report called ["Project Cyclops: a Design Study of a System for Detecting Extraterrestrial Intelligent Life"][project-cyclops-1972-report]. This report was digitised by NASA in 2013 and is publicly available online. 

While the authors of the report declared the study as "extremely preliminary" and "a rough set of estimates", it became known as "The Bible of SETI" and influenced SETI research for decades, in particular by reaffirming that radio wavelengths should be prioritised.

Since this report is so long, I have split my notes into two posts. Here are my notes from reading the first part of the original report, which contains introductory material on the origin, evolution and survival of life in the universe, reasons for searching for and methods of contact with extraterrestrial intelligence. The second part of the report presents details of the Cyclops system and you can read my notes on this here:

[Project Cyclops - Part II][project-cyclops-1972-notes-ii]

You can find my notes on other classic SETI papers in my [roundup of the technosignatures literature][technosignatures-literature].

## Life in the universe
Following a brief introductory chapter, chapter 2 of the report discusses why the debate had moved on to the best way to discover extraterrestrial civilisations, rather than whether or not they exist. 

We can presume technologically advanced extraterrestrial life is prevalent in the universe given that:
- Planetary systems are expected to be common (none had yet been discovered at the time the report was written)
- The origin of life on Earth was governed by universal laws of physics and chemistry
- The materials required for life are common in the universe
- Evolution by natural selection is likely to happen wherever there is life (although intelligence, and therefore technology, is not necessarily an inevitable product of natural selection).
- As far as suitability for life, Earth is probably average, rather than special, in the universe 
- Extraterrestrial technology will be shaped more by physical laws than by the nature of those designing them

Interestingly, the following sentence appears in the section on the origin and evolution of matter: 
> "The universe contains over a billion galaxies, or, in all, more stars than there are grains of sand on all the beaches of Earth." 

The metaphor used here was made famous by Carl Sagan who used it in his book/TV series [Cosmos][cosmos] in the early 80s. This quote inspired me to [use sand to show my children how many stars there are in the universe][palebluemarbles-stars-sand] (posted in my astrobiology blog for children/parents). The same chapter of the report references the book "Intelligent Life in the Universe" published in 1966 by Sagan and Shklovskii (a "fundamental and lucidly written review") so perhaps the metaphor originates there - I have ordered the book from my local library.

Another idea that caught my attention in this section was that, in the same way an intelligent being is able to contemplate its own existence, the universe is "contemplating itself through the minds and eyes of the living beings evolved by the universe itself".

### Stellar evolution
Our galaxy has billions of stars. Different types of stars affect their orbitting planets in different ways, and some make life on them highly unlikely. We can narrow down our search for extraterrestrial intelligence by learning what stars are best to search.  

Most stars are older and smaller than the Sun (larger stars are less likely to be born due to the way mass is distributed in molecular clouds - although more recent data suggests they are more common than was previously thought).

The very oldest stars cannot have earthlike planets since heavy elements were not present at the time (they form in stars). These stars dominate in the halo and nucleus of the galaxy; young stars dominate in the disk and the youngest stars are in the spiral arms. In the nucleus, the density of stars is about a hundred times higher than in our solar neighbourhood, but it contains only 10% of the total stellar mass.

Our solar neighbourhood is not special - it is a typical environment of the galaxy. The sun, together with most stars in our neighbourhood, orbits the galactic centre once every 240 million years and in the process crosses all components of the spiral arms. Stars born in the spiral arms (the "maternity wards of the galaxy" with a high density of gas and dust) drift out of the arms and mix with older stars. This mixing of stars means there is nothing special about our solar neighbourhood.

The authors of the Cyclops report recommended we confine our search to main sequence stars due to the catastrophic affect leaving the main sequence has on planets. Highest priority should be given to F, G and K main sequence stars (25% of all stars: stars are classified by their spectral types, from hottest/bluest to coolest/smallest/oldest/reddest: O, B, A, F, G, K, M; the Sun is a G type star). 

The vast majority of stars live long enough for intelligent life to evolve if the rates of evolution are the same as on Earth. But stars that are hotter than F type stars do not and so can be excluded.

M main sequence stars should also be excluded since for a planet to be habitable it would need to be close to the star (since the star is cool) and the resulting gravitational force from the star would prevent the planet from rotating (it would become "tidally locked"), which would cause the atmosphere to freeze on the dark side. M stars are the most common type in the Universe. Many exoplanets have been discovered around M type stars since this report was published and they are not necessarily ruled out in the search for life these days. 
  
### Exoplanets and ecospheres
At the time this report was written, no exoplanets had been found and direct imaging was thought to be impossible. The wobbling of some stars was used as indirect evidence for their existance. [Barnard's star][barnards-star] (which is an M type star and the nearest star after the stars in the [Alpha Centauri][alpha-centauri] system) was thought to have more than one planet and the Cyclops report gives details on this but so far no planets around this star have been found.

The report also contains a section on "ecospheres", which are defined as "the region surrounding a star within which planetary conditions can be right to support life". This is now more widely known as the ["habitable zone"][habitable-zone] or "circumstellar habitable zone" (CHZ). Interestingly, the report states that the factors responsible for suitable atmospheric evolution (Earth's atmosphere was generated by outgassing from volcanoes followed by the capture of CO$$_2$$ by the oceans and life, which prevented a runaway greenhouse effect) may be more limiting than the habitable zone . 

Over half of all planetary systems were thought to have at least one favourably situated planet. The habitable zone is expanded for larger/hotter stars but the number of planets in this zone was estimated to be the same due to [Bode's law][titus-bode], which predicts that each planet is about twice as far from its star as the next closest planet (although the positions of the planets in our solar system beyond Uranus do not fit with this law and there is currently no theoretical basis for it; later analysis by Blagg found 1.73 fit much better)

### The origin and evolution of life and technology
Exactly how life originated on Earth is still an open question but it began with a soup of molecules that gained the ability to replicate. Evolution through natural selection then favoured the features with the highest survival advantage. Over time this led to the information carrying molecules DNA and RNA, cells, photosynthesis, multicellularity, flowers, flight, nervous systems, skeletons, intelligence and, for humans, language, writing, technology, science, industrialisation and civilisation. 

Human technology has advanced rapidly and as the report states:
> "The boundary between the living and nonliving (machines) is becoming less clear in any absolute terms".

The probability of the exact sequence of events that led to technologically advanced human civilisations is vanishingly small but there are alternate routes that would produce statistically indistinguishable outcomes. The report concludes that instead of asking if the exact conditions that produced the exact sequence of events on Earth exist elsewhere we should ask "whether the forcing functions are present and whether enough alternate routes exist", proposing that a variety of environments would lead to the highest chance of a technologically advanced civilisation emerging.

### How many other advanced civilisations are there?
This section presents theoretical calculations for estimating how the fraction of the present number of candidate sites for life changes over time. These use the rate of F, G and K main sequence star formation in the galaxy (which is proportional to the density of interstellar dust) together with estimates for the time taken for technologically advanced life to evolve (4.5 billion years) and their longevity (1 billion years: this is much more optimistic than previous estimates by [Drake][drake-1965-notes] {% cite  drakeRADIOSEARCHINTELLIGENT1965  %} or [Hoerner][hoerner-1961-notes] {% cite  hoernerSearchSignalsOther1961  %}). This results in a very interesting plot (Figure 2-10) that shows that the galaxy may have been populated with advanced civilisations for up to 6 billion years and that they were more common in the past than they are now. 

The report goes on to present the famous [Drake equation][drake-1965-notes] {% cite  drakeRADIOSEARCHINTELLIGENT1965  %}, which it says has been described as "a way of compressing a large amount of ignorance into a small space", and to show that the number of communicative civilisations in the galaxy right now is approximately equal to the average longevity (as described by [Drake][drake-1965-notes]). This assumes the evolution of life is inevitable on a planet suitable for life.

### The probability of interstellar communication
The next section presents estimates for how many stars we need to search and how long it will take for us to find an extraterrestrial civilisation. 

The authors started with a statement that to have a 63% chance of success we need to search 1/p stars, where p is the probability that a random star hosts another civilisation. My probability theory is a bit rusty so I had to look up where the 63% came from: it's a result of modelling the detections as a poison distribution.

- If detecting another civilisation is an event that occurs at a fixed rate independently of any previous detections (i.e. we assume that if we discover one civilisation it will not influence the likelihood of us detecting another) then the probability of a given number of detections in a fixed interval, given a fixed rate of occurrences, can be modelled by a [poisson distribution][poisson-distribution-wikipedia]
- The probability of $$k$$ events occurring is given by the formula $$\frac{\lambda^ke^{-\lambda}}{k!}$$, where $$\lambda$$ is the expected rate of occurrences
- To work out the probability of at least one event occuring in a fixed interval we calculate the probability of no events occurring ($$k = 0$$) when the expected frequency of occurrence ($$\lambda$$) is 1 in that interval and subtract it from 1:

$$ 1 - \frac{1^0e^{-1}}{0!} = 1 - \frac{1}{e} \approx 1 - 0.37 = 0.63$$

- The interval in this case is the number of stars searched, which is equal to $$1/p$$ (since $$p$$ is the probability that one star in the number searches has a communicative civilisation)

Using 1000 seconds (16 minutes) to search each star, the report gives an estimated minimum time of 560 years needed for us to detect another civilisation if contact with one does not change the probability of contact with another. I suspect that with present and/or future telescopes, and once we have a suitable algorithm for detections, searching each star will be much faster. 

The report reduced this number to a range of 1 day to 4 months with reference to the "feedback effect" that [Von Hoerner][hoerner-1961-notes] {% cite  hoernerSearchSignalsOther1961  %} proposed would happen if advanced civilisations cooperated to contact additional civilisations, and proposes that interstelllar communication would spread rapidly through the galaxy once initiated. 

**Project Cyclops was intended to show that humanity has the technological capability to join an interstellar network of communication.**

## Reasons for the search
Chapter 3 of the Cyclops report lays out the rationale for searching for extraterrestrial intelligence. The authors proposed that it is worth doing in parallel to solving the world's ecological problems (we have made shockingly little progress on this in the half century since this report was written) and that the two are related since the longevity of a civilisation depends on it not destroying itself and so it may help us to discover whether or not others have succeeded. 

The report lists some of the many open questions that might only be answered by discovering life elsewhere in the universe. These include:

- How prevalent is life in the universe?
- Is there an alternative to DNA?
- What is the typical longevity of a planetary culture?
- Are biological morphologies sensitive to small differences in the environment or is evolution highly convergent?
- Does life modify the universe?  

The chapter also summarises a few ideas for how contact with another civilisation might benefit us or pose a risk. The major benefit would be helping us with our own self-preservation and most of the risks are limited:
- Exploitation is unlikely:
  > "compassion, empathy and respect for life correlate positively with intelligence, though counter examples are not hard to find"
- Invasion is unlikely since interstellar travel is so expensive
- Subversion can be avoided with appropriate caution
- Cultural shock is possible:
  > "historically contact between two terrestrial cultures has usually, if not always, resulted in the domination of the weaker by the stronger"
  but the authors argued that this is unlikely to happen via radio only, which will take so long that we will have time to adapt

The chapter concludes with the opinion that the benefits greatly outweigh the risks and that the risks are only present if we choose to respond to a signal (although we are already detectable to about 100 light years away).

## Methods of contact
The fourth chapter of the Cyclops report gives details on the four main methods of contacting extraterrestrial intelligence: interstellar travel; interstellar probes; serendipidous contact; and sending/receiving signals. 

### Interstellar travel
The limiting factor for interstellar travel is the mass ratio (what mass of fuel is required to achieve a certain speed compared to the mass of the ship - less fuel means a more efficient rocket). At the time of the report, the fastest spacecraft would take 40,000 years to travel 4 light years to the next star (alpha Centauri). This makes interstellar travel impractical until we can develop "some radically new form of propulsion". 

If we could use nuclear fusion to power the ship then we could reduce the time for a round trip to 80 years. 

The report presents calculations for the best possible rocket according to the known laws of physics - i.e. a photon rocket which uses the annihilation of matter and antimatter to create energy - and concludes that a return trip could be done in about 10 years close to the speed of light but would require 33,000 tons of fuel at a cost (in the 1970s) of one million billion dollars of nuclear fuel. And that is just one trip of about 10,000 that would be required to explore the galaxy and have a high chance of finding another civilisation. The energy expended in one trip would keep a beacon operating for over 30 million years. In addition the waste heat produced on the journey and absorbed by the ship would require a surface area of 2589 km$$^2$$ for cooling and at these high speeds any collision with interstellar dust would be catastrophic. 

The report mentions other proposed methods of propulsion but, due to the challenges and particularly the expense, concludes that interstellar flight is "out of the question not only for the present but for an indefintely long time in the future".

### Interstellar probes
Bracewell proposed that an extraterrestrial intelligence would send [probes to other stars][bracewell-1960-notes] {% cite  bracewellCommunicationsSuperiorGalactic1960  %} but the authors of the report argued that it would be too expensive, even for an advanced civilisation, to "bug" all the stars within 1000 light years.

### Serendipidous contact
Dyson {% cite  dysonSearchArtificialStellar1960  %} suggested that we search for unusual amounts of infrared radiation from stars that might be due to waste heat emitted by megastructures created by an extraterrestrial civilisation around their star ([Dyson spheres or Dyson swarms][dyson-1960-notes]). The participants of Project Cyclops did not support a search strategy focussed on Dyson spheres, arguing that a civilisation capable of such engineering is more likely to construct a beacon and search system first. Moreover, we would not be able to tell whether excess infrared was due to a megastructure or dust around a star. The authors concluded that the chance of accidental contact is negligable. 

### Electromagnetic signals
Chapter 4 concludes with the statement that:

> "almost certainly electromagnetic waves of some frequency are the best means of interstellar communication - and our only hope at the present time". 

Using particles other than photons are ruled out since they require more energy to generate and are more likely to be deflected by magnetic fields or absorbed by interstellar dust.

## Communication links using electromagnetic waves
Chapter 5 presents calculations and background information to show that, with two antennas (a transmitter/radiator and a receiver/collector of electromagnetic waves) pointing in the right direction at the right time (i.e. once we have established a link with another communicative civilisation) communication using electromagnetic waves is possible over interstellar distances. 

The authors compared several different hypothetical systems that use microwaves, infrared and near-optical wavelengths and antennae that are at or just beyond the capabilities of the technology of the time in order to determine what frequency window would be best for communication. 

They also went into detail on the expected noise levels and concluded that a signal to noise ratio of 6.06 is needed to avoid missing the signal. The noise of a radio receiver is comparable to the noise of a photodetector (photons can be detected directly at optical wavelengths but this is very difficult for lower energy radio photons).

- For fixed antenna areas, the transmission increases with the square of the frequency
- Noise in a receiver also increases with frequency
- Using a synchronous (homodyne) detector (which uses the same frequency as the transmission) would maximise the signal to noise ratio
- Once the limit of the transmitter's power is reached the only way to increase the energy received is to increase the signal duration, which narrows the bandwidth (the signal duration is inversely proportional to the bandwidth of a signal) and the authors expected this to result in the use of highly monochromatic (narrow band) signals for interstellar communication.

### Microwave window
There is a window in the electromagnetic spectrum that is subject to the least noise from the galactic and universal background radiation as well as the least quantum noise and the least absorption by Earth's atmosphere. This window lies between 1 and 100 GHz i.e. in the microwave region of the spectrum.

The authors noted that the noise from the host star does not pose a serious problem for detecting microwaves with antennas up to 10 km in diameter and for stars beyond 10 light years. The report gives temperature values (table 5.2) for the quiet and active sun, which were missing from the [Cocconi and Morrison paper][cocconi-morrison-1959-notes] {% cite  Cocconi1959  %}, which used similar equations to calculate a similar optimum frequency of interstellar communication. 

### Doppler drift
The relative movement of a source and a receiver (towards or away from one another in space) causes the Doppler effect, i.e. a shift in the frequency of an electromagnetic wave (to higher frequency when moving towards and lower frequency when moving away). Since Earth and an exoplanet are rotating about their own axes and their stars, the Doppler effect in any signal sent from them would change over time - this is known as Doppler drift. The authors of the Cyclops report estimated that optical systems would require tunability over a $$\pm$$300 GHz range and infrared would require $$\pm$$30 GHz. 

### Microwave over optical
The authors summarised why they thought an interstellar communication link would favour the microwave region of the electromagnetic spectrum, rather than the optical region. Microwave systems have:

- Cheaper and more durable collecting surfaces (optical requires polished surfaces)
- More range for the same power
- Lower Doppler shifts and drifts
- All-weather capabilities (optical is unusable in cloudy weather)

They conclude with:

> "...we believe that if lasers had been known for the last hundred years and microwaves had only recently been discovered, microwaves would be hailed as the long sought for answer to interstellar communication"

and show that existing microwave antennas could be used to communicate over interstellar distances of 100 (at 100 bits/sec) to 1000 (at 1 bit/sec) light years and arrays of one to several kilometers would allow millions of bits/sec communication.

## The central problem
While chapter 5 examined the practicalities of two-way communication over interstellar distances, it assumed that the direction and frequency of transmission was already known. Chapter 6 deals with the main problem of SETI: finding a signal in the first place. This requires searching the sky and the electromagnetic spectrum for artificial signals. How we do this depends on how far out into space we must search, which in turn depends on the probability that a random star hosts a communicative civilisation. This probability is completely unknown but, as the authors of the report argued, we have to make some approximation in order to get started.

### How far must we search?
The density of stars is higher in the galactic plane and decreases as distance from the plane increases. The report quotes a density of $$5.4 \times 10^{-4}$$ F to K main sequence stars per cubic light year and adjusts this density according to distance from the galactic plane. Up to about 500 light years from the sun, the relationship between the distance and the number of stars follows a cube law.

If the probability that a signal is radiating from a planet around a star is 1 in 1000 (e.g. if a civilisation has been radiating signals for millions of years (we have only been radiating signals for 100 years)), then we need to search 1000 stars to have a 63% success rate (3000 for a 95% success rate), which means we have to detect signals up to 100 light years away.

If the probability is lower (e.g. 1 in a million: a civilisation that has been radiating beacons for 10,000 years) then we have to search a million stars, which would require searching up to 1000 light years away from the Sun.

Given the uncertainty in how many stars, and therefore what distance we need to search, the authors of the report recommended starting with a modest search system that can be expanded over time, working our way up from 100 to 1000 light year range. They also pointed out that searching several stars simultaneously "does not appear too feasible" since the number of directions an antenna must be pointed to cover the whole sky is high and increases with the diameter of the antenna and the frequency of the signal.

### How far can we search?
The range for our search is limited by noise - once the signal to noise ratio equals one we cannot distinguish between signal and noise. This gives us the maximum distance we can search, which is proportional to the diameter of the receiving antenna and the square root of the effective power of the transmitter and inversely proportional to the square root of the bandwidth and the temperature of the source (higher temperature leads to more noise).

### What frequency range should we cover?
Even if we know what frequency to look for we have to broaden the band to account for Doppler drift from:
- The relative velocity of the star to the Sun (maximum of 60 km/s for relevant stars, according to the report) which would result in a fixed offset of maximum $$\pm 2\times 10^{-4}$$ (0.02%).
- Planetary motion around a star (max $$\pm10^{-4}$$ (0.01%) for Earth) varying sinusoidally with time
- Planetary rotation about its axis (max $$\pm1.5 \times 10^{-6}$$ (0.00015%) for Earth) varying sinusoidally with time

As the frequency of the signal increases so does the band that must be searched to account for these drifts (Table 6-1 in the report gives estimates ranging from 1.14 MHz for the 21 cm hydrogren line to 230 GHz for optical which would result in drift rates of 1.4 Hz/s and 280 kHz/s respectively), which adds further reason to use the microwave region of the spectrum rather than the optical. Furthermore, as drift rates increase, the maximum range (signal to noise ratio of 1) decreases. 

Other reasons given in the report for favouring the microwave region of the spectrum include:
- Greater collecting area for the narrowest beam, with a lower cost per unit area
- Less stringent frequency stability requirements
- More freedom from O$$_2$$ and H$$_2$$O absorption

#### The water hole
The authors proposed focussing the search on the region between 1 and 3 GHz. They discussed the hydrogen line (this would require about 3 MHz of bandwidth) but argued that choosing a single frequency would lead to jamming ourselves if it is used for both transmission and reception simultaneously. They suggested a broader band that does not contain spectral lines (since they interfere with radio astronomy and create noise) and is not below the hydrogen line (since this would interfere with observations of red-shifted galaxies and has more background noise) and landed upon the band from the hydrogen line to the hydroxyl line (1420 - 1662 MHz), which has become known as the water hole.

> "The resonances of the dissociation products of water is ideally situated and an uncannily poetic place for water-based life to seek its kind. Where shall we meet? At the water hole, of course!"

### For how long should we search?
The authors of the report estimated that to search the entire sky in order to detect the signal from a beacon that is transmitted in our direction for 1 second per day the search with a 1 Hz bandwidth receiver would take 30 million times the age of the galaxy. To reduce this time to 50 years we must:
- Narrow down the search to the 1 million most likely stars within 1000 light years
- Search all likely channels of the spectrum simultaneously
- Search only for beacons that are always on (assuming another civilisation is trying to attract the attention of others) and/or "leakage" radiation from the nearest stars (uncertain longevity and lower power than beacons)

### Properties of beacons
The authors of the report went on to examine the likely properties of an extraterrestrial beacon. They argued that a beacon will be:

- Omnidirectional (to maximise range)
- High-powered (to maximise range)
- Transmitting continuously (to maximise chance of detection)
- Extremely monochromatic/narrow band (to allow longer signal duration)
- Circularly polarised (left or right-handed) (to save time and cost of detection compared to linearly polarised waves)
- Information bearing (to save time)

### Anticryptography
The final section of chapter 6 discusses what kind of message we should expect to receive with the argument that any civilisation that wants to communicate with another will make it as easy as possible to decipher a message and will include how to respond. Since they are also likely to posess vision the message is likely to contain pictures.

## Summary
The Cyclops Project was hugely influential on SETI research that followed it and represented the first large-scale coordinated effort of experts in the field at the time to tackle its central problem: detecting an extraterrestrial signal when we don't know where to look.

The first part of the resulting report presents background material and calculations that lay the foundations for their proposed system for the detection of signals from extraterrestrial intelligence. It emphasised the preferrence of the microwave region of the spectrum, with detailed calculations to back this up, and proposed the water hole band to target in the first instance. Given the uncertainty in the probability of another technologically advanced civilisation emerging elsewhere, their longevity and the power of their transmitters, the report could not present any firm conclusions on the number of stars we must search but suggested starting with the nearest 1000 and then scaling up to the nearest 1 million (within 1000 light years) with a search system that can be scaled up. The report also recommends restricting the search to F to K main sequence stars.

The rest of the report details the design, requirements and costs of this system and I have documented this in my [next post][project-cyclops-1972-notes-ii].


## References

{% bibliography --cited %}

[alpha-centauri]: https://en.wikipedia.org/wiki/Alpha_Centauri
[asee]: https://www.asee.org/
[barnards-star]: https://en.wikipedia.org/wiki/Barnard%27s_Star
[bernard-oliver]: https://www.seti.org/bernard-m-oliver-1916-1995
[bracewell-1960-notes]: https://open-research.gemmadanks.com/literature/communications-superior-galactic-communities/
[cocconi-morrison-1959-notes]: https://open-research.gemmadanks.com/literature/search-for-interstellar-communications/
[cosmos]: https://www.imdb.com/title/tt0081846/
[drake-1965-notes]: https://open-research.gemmadanks.com/literature/drake-equation/
[dyson-1960-notes]: https://open-research.gemmadanks.com/literature/dyson-spheres/
[habitable-zone]: https://exoplanets.nasa.gov/search-for-life/habitable-zone/
[hoerner-1961-notes]: https://open-research.gemmadanks.com/literature/waiting-times-and-longevity/
[john-billingham]: https://www.seti.org/john-billingham-1930-2013
[nasa-ames]: https://www.nasa.gov/ames
[palebluemarbles-stars-sand]: https://www.palebluemarbles.com/count-the-stars-in-grains-of-sand/
[poisson-distribution-wikipedia]: https://en.wikipedia.org/wiki/Poisson_distribution
[project-cyclops-1972-report]: https://ntrs.nasa.gov/citations/19730010095
[project-cyclops-1972-notes-ii]: https://open-research.gemmadanks.com/literature/project-cyclops-part-ii/

[technosignatures-literature]: https://open-research.gemmadanks.com/literature/technosignatures-literature-roundup/
[titus-bode]: https://en.wikipedia.org/wiki/Titius%E2%80%93Bode_law


<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>