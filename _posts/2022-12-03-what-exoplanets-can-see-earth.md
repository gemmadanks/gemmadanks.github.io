---
title: "What exoplanets can see technosignatures from Earth?"
date: 2022-12-03 T16:19:00
categories:
  - literature
tags:
  - research
  - astrobiology
  - technosignatures
  - exoplanets
  - literature
  - summary
  - seti
---

A recent paper in [Nature][nature] {% cite kalteneggerPresentFutureStars2021a %} caught my attention because it reversed my perspective on the topic. Rather than focussing on whether we can see life elsewhere, it asks whether life elsewhere can see us. Here are my notes from reading this paper. 

I am tracking all of the papers I've read and want to read on this topic in this [roundup of the technosignatures literature][technosignatures-literature].

# How do we find exoplanets?
Our search for exoplanets has largely relied on detection via the [transit method][transit-method]. This is where we measure a dip in the brightness of a star over time due to a planet passing in front of it. The resulting light curve can tell us the size of the planet and its orbit. This is how astronomers found thousands of exoplanets with NASA's [Kepler Space Telescope][kepler] and how they are discovering thousands more with the [Transiting Exoplanet Survey Satellite][tess]. 

# Is Earth visible from exoplanets? 
Finding exoplanets, particularly habitable ones, helps us figure out where to search for other intelligent life. But what if an alien intelligence is also looking at the stars and trying to answer the same question? Could they detect Earth transiting the Sun and list our planet as one of their candidates for hosting extraterrestrial intelligence? If so, it might prompt them to send us a message, which we could intercept if we know where to look.

## Stars that can see Earth's transit across the Sun
1,402 stars are currently in the region of space from which Earth could be seen transiting the Sun {% cite kalteneggerPresentFutureStars2021a %} (known as the Earth Transit Zone (ETZ) {% cite hellerSearchExtraterrestrialIntelligence2016 %}).

## Exoplanets that can see radio signals from Earth
46 of the 1,402 stars in the ETZ are close enough (within 100 light years) that they could also detect radio waves emitted by human technology. These are estimated to host 29 potentially habitable planets. More will enter the ETZ in the future. Most remain in the ETZ for over 1000 years. 

## Exoplanets that can detect other atmospheric technosignatures on Earth
Humans have had a potentially detectable impact on Earth's climate for over 200 years (since the invention of the steam engine and beginning of the industrial revolution). These atmospheric [technosignatures][technosignatures] from Earth have already reached 1,424 stars in the ETZ. 

## Exoplanets that can detect life on Earth
[Biosignatures][biosignatures] from Earth have existed for over a billion years (since the [Great Oxidation Event][goe]) so any planet that has passed through the ETZ in the last billion years could have identified Earth as a candidate for hosting life. 

# Data availability
We are continuously gathering more and more detailed information about the Universe. New missions and new technologies allow us to see what we haven't been able to before. This means that our statistics and measurements of different types of stars and exoplanets are always changing and this opens up for more questions to be answered. 

Previous work {% cite kalteneggerWhichStarsCan2020 %} had looked at the number of stars that could see Earth transiting the Sun but Kaltenegger and Faherty {% cite kalteneggerPresentFutureStars2021a %} were able to use more [recent and detailed data][gaia-dr3] from the [European Space Agency’s][esa] [Gaia mission][gaia]. 

Gaia measures the positions and distances (and many other characteristics) of over 1.3 billion stars in our stellar neighbourhood with high precision. It has released the "Gaia Catalogue of Nearby Stars" (GCNS), which contains data on the most (302,197) stars within a distance of 326 light years from the Sun. 

The set of nearby stars from the GCNS formed the basis for the latest analysis of stars in the ETZ. The authors were also able to account for the changing positions of the stars over time and so were able to include stars that had seen Earth in the past and ones that would see our planet in the future. [The full list of stars is available on GitHub][suppl]. 

# Summary
This paper answers an important question in the search for intelligent life elsewhere in our stellar neighbourhood: who can see us? It allows us to narrow the search for extraterrestrial communications to those who can see we are here.

# References

{% bibliography --cited %}

[biosignatures]: https://open-research.gemmadanks.com/notes/exoplanet-biosignatures/
[esa]: https://www.esa.int/
[gaia]: https://sci.esa.int/web/gaia
[gaia-dr3]: https://www.cosmos.esa.int/web/gaia/early-data-release-3
[galactic-neighbourhood]: https://www.icc.dur.ac.uk/~tt/Lectures/Galaxies/LocalGroup/Back/superc.html
[goe]: https://en.wikipedia.org/wiki/Great_Oxidation_Event
[kepler]: https://www.nasa.gov/mission_pages/kepler/overview/index.html
[my-research-process]: https://open-research.gemmadanks.com/planning/my-research-process/
[nature]: https://www.nature.com/
[suppl]: https://github.com/jfaherty17/ETZ
[technosignatures]: https://open-research.gemmadanks.com/notes/technosignatures/
[technosignatures-literature]: https://open-research.gemmadanks.com/literature/technosignatures-literature-roundup/
[tess]: https://tess.mit.edu/
[transit-method]: https://exoplanets.nasa.gov/faq/31/whats-a-transit/
[why-technosignatures]: https://open-research.gemmadanks.com/planning/my-next-research-topic-technosignatures/