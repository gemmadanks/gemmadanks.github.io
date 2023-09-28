---
title: "A search strategy for finding extraterrestrial radio beacons"
date: 2023-05-22 T14:26:00
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

Building on the work of the [Cyclops Project from 1971][project-cyclops-notes-part-i], Robert Dixon (a member of the signal processing group during the Cyclops Project) from Ohio State University Radio Observatory published a paper in 1973 that used the principle of anticryptography and the assumption of mediocrity to predict the characteristics of a beacon transmitted by an extraterrrestrial intelligence for the purpose of initiating communication with other civilisations, and how best to go about detecting it {% cite  dixonSearchStrategyFinding1973  %}.

Here are my notes from reading this paper. You can find my notes on other classic SETI papers in my [roundup of the technosignatures literature][technosignatures-literature].

## Anticryptography
If an extraterrestrial civilisation were to transmit a beacon for the purpose of initiating contact with another civilisation, they would try to make the message as easy as possible to detect and decipher. This has been called the principle of anticryptography.

## Mediocrity
We assume that our civilisation is typical and that another civilisation would have a similar knowledge of the laws of physics and similar (or more advanced) technology.

## Unknown dimensions
To make a beacon as easy to detect as possible the sender would minimise the number of unknown dimensions the recipient would have to search and for any bounded continuous range of values they would choose one extreme (e.g. zero), rather than something arbitrary value in the middle. 

### Distance
In the first instance we should limit our search to stars within 1000 light years of the Sun since with increasing distance there is a decrease in: the signal intensity; our knowledge of detailed stellar characteristics; and the possibility of two-way communication. Longer travel times for the message also require greater cultural longevity of a civilisation.

There is a very nice figure in the paper that shows how small this sphere of 1000 light years is compared to our galaxy and 'gives perspective to the fact that we are still only searching in our own "backyard"'

### Direction
Due to our lack of knowledge on the characteristics of the stars further than 100 ly away, Dixon suggested searching in all directions, possibly concentrating on where stellar densities are highest. The authors of the Cyclops report previously suggested that developing a list of candidate stars was the first step towards beginning the search (we should rule out those that are unlikely to host habitable planets) {% cite  ProjectCyclopsDesign1972  %}. We have a lot more information about the stars today and also their planets so we can choose the direction of the search more easily.

### Time
To maximise the probability of detection a sender will transmit a beacon continuously in all directions, rather than periodically towards specific stars. 

### Bandwidth
To maximise range for a given power a beacon will transmit at a narrow bandwidth (a value close to zero according to the principle of anticryptography).

### Signal rate
It should take only a small fraction (e.g. 1%) of the recipient's lifetime to receive any message in a signal. In addition we can assume that any extraterrestrial intelligence would account for the rotation of a recipient's planet, which would ideally allow a full message to be received within half a rotation. Dixon permitted an order of magnitude difference and gave an estimate of one message every 1.2 - 120 hours for the message rate. 

The signal rate (how many bits per second) should also be as slow as possible to make it easier to detect and Dixon argued that 0.1 bits per second is the lower practical limit. He estimated a signal rate of 0.01 to 1 bits per second, which is equivalent to a period of 1-100 seconds. Interestingly, Dixon noted that this is in a similar range to that of pulsars (0.01 - 10 seconds) and argues that this might be a good signal rate to use since it might be discovered accidentally by astronomers looking at pulsars.

### Polarization
Dixon reaffirmed that a circularly polarised signal is the most likely since it removes another unknown and is not affected by the interstellar medium. Circular polarisation can be left- or right-handed. Dixon proposed that switching between these two states could provide the means to encode a binary signal. 

### Modulation
In order to carry information the signal will be modulated by introducing time variations in the amplitude, phase, frequency or polarisation. Switching between two states (binary modulation) is the most effective option for maximising range and is best to have two 'on' states (-1 or 1) rather than on/off (0 or 1) since any 'off' state could be missed.

Dixon ruled out amplitude modulation (since there can be no negative amplitude), frequency modulation (since it introduces another unknown) and phase modulation (phase is not usually measured and so is least likely to be detected accidentally). He argued that switching between left- and right- circular polarisation is the logical choice since it removes the need to choose one or the other. 

Modulating polarisation is uncommon in our communication on Earth. We mostly use linearly polarised signals. Dixon pointed out that we could use a Dicke radiometer system, which discriminates against linearly- and un- polarised signals and would therefore reduce interference from both terrestrial radio signals and natural radio sources. 

### Frequency
Dixon reiterated the consensus at the time on what frequency to search:

> "It is generally agreed that the optimum frequency range for interstellar communications lies between approximately 1 and 10 GHz."

He went on to argue that the hydrogen line, as proposed by [Cocconi and Morisson][cocconi-morrison-1959-notes] {% cite  Cocconi1959  %}, is the best choice of frequency to search since it is the lowest and strongest frequency line in the microwave window and so most likely to be well-known. Hydrogen is also the lightest and most abundant element in the universe. He addressed the arguments against the use of the hydrogen line that had emerged since it was first proposed:

- Hydrogen emission itself may drown out any signal
  - Accounting for Doppler shifts at both the transmitter and receiver ends, including that from galactic rotation (larger than for planetary rotation and revolution around its host star), would mean the receiver is tuned to frequencies that are outside the band of hydrogen emission. This requires an omnidirectional beacon to simultaneously transmit a different frequency in different directions. Dixon suggested several ways this could be done including using:
    - Multiple transmitters for different parts of the sky
    - A satellite that orbits in a stationary position relative to the galactic centre
    - Frequency scanned arrays to remove Doppler shifts directly. 
  
  Dixon also argued that since the receiver frequency would be changed over time to account for Doppler shift due to Earth's rotation, terrestrial interference could be easily identified since it would not have this frequency variation.
- Absorption by interstellar hydrogen may block signals
  - Most absorbing regions are further than 1000 ly away
  - Absorbing regions are highly concentrated along the galactic plane
  - Absorption bandwidth is small
  - The Doppler correction method Dixon proposed would remove most hydrogen absorption effects
- Transmissions at hydrogen line frequency may cause interfere for astronomers studying hydrogen emissions (transmissions at this frequency are not allowed on Earth for this reason)
  - Transmission could be done by satellite
  - Communication with other civilisations may be valued higher than hydrogen line observations
  - Doppler correction would mean transmitting a slightly different frequency

Dixon noted that a frequency search would still be required with his proposed Doppler-shift correction method since (at the time of writing) we have a 10% error margin in our knowledge of our own galactic rotation velocity. This corresponds to a frequency uncertainty up to $$\pm $$125 kHz.

Dixon concluded with the following:

> The Principle of Anti-Cryptography leads one to believe that interstellar beacons will transmit omnidircctionally, at a doppler-corrected hydrogen line frequency, using binary sense-switched circular polarization modulation, with switching rates of the order of 1 sec.

## Summary
In this paper, Dixon proposed a search strategy for finding a communicative extraterrestrial intelligence under the assumption that they are transmitting a signal that is as easy as possible to detect and decipher (the principle of anticryptography). This means choices of continuous values are close to one extreme rather than an arbitrary value in the middle. He looked at each unknown dimension and concluded that a signal is most likely to be circularly polarised and carry information by switching between left- and right- handedness. The information would be sent at a rate that allows one full message to be received every half rotation of a typical terrestrial planet and the signal rate would be on the order of around 0.01 - 1 bits per second to increase the likelihood of detection. 

Dixon argued strongly that a signal would most likely be at the frequency of the hydrogen emission line and proposed that the sender and receiver of a signal should correct for Doppler shifts due to the rotation and revolution of their own planet and their own rotation around the galactic centre. This would make common arguments against using the hydrogen line frequency irrelevant since the actual frequencies transmitted and received would be outside of this band and would vary in frequency with position in the sky and time.


## References

{% bibliography --cited %}
[cocconi-morrison-1959-notes]: https://open-research.gemmadanks.com/literature/search-for-interstellar-communications/
[project-cyclops-notes-part-i]: https://open-research.gemmadanks.com/literature/project-cyclops-part-i
[technosignatures-literature]: https://open-research.gemmadanks.com/literature/technosignatures-literature-roundup/

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>