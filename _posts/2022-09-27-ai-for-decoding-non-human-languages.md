---
title: "AI for decoding non-human languages"
date: 2022-09-27 T14:00:00
categories:
  - notes
tags:
  - planning
  - ai
  - decisions
  - language
  - non-human
---

A.I. has become incredibly powerful for translating human languages. Could it be used to glean information from non-human languages? The impact of understanding non-human animal communication would be enormous. We would have the knowledge and the additional motivation to reduce their suffering on a global scale and improve conservation efforts. We would also be better prepared for any extraterrestrial messages that we find.

This topic came out top of [my decision matrix][choosing-research-topic] for deciding what to work on next based on impact and how well it matches my skills and interests. I am spending one day on each of my top 5 topics to learn a bit more before choosing which to focus on:

1. **AI for translating unseen languages**
2. [Extraterrestrial technosignatures][technosignatures]
3. [Recognising AI sentience][ai-sentience]
4. [Biosignatures][biosignatures]
5. [AI misuse: pathogenic DNA][ai-misuse-pathogenic-dna]

Here are my notes resulting from a day spent learning about the current status of using A.I. to decode non-human languages.

## Existing work
Interest in this topic is high and several projects are already underway.

- The [Earth Species Project][esp] is a species-agnostic open-source collaborative project that aims to decode non-human animal communication. 
- [Project CETI][ceti] aims to translate communication betweeen sperm whales. The roadmap for this includes data collection using robotics, data processing and machine learning to extract meaning from sounds collected.
- [Elephant voices][elephant-voices] and [Elephant listening project][elephant-listening-project] collects behavioural and sound data from elephants.

## Neural machine translation
There is an increasing number of neural networks that are able to translate from one human language to another with high accuracy. These seqence-to-sequence (seq2seq) models have two parts that together do the translation: an encoder extracts meaning from the input language and a decoder outputs this meaning in the target language. A mechanism is also included for teaching the network what words to pay the most attention to. The best results at the moment come from [transformer models][google-ai-transformer-blog], largely because the attention mechanims work better in transformers than on the earlier models that used recurrent neural networks (RNNs). This is because the transformer models do not take the words sequentially but instead look at them in parallel.

Training a neural machine translation model is usually supervised and requires a lot of labelled data. The network has to 'see' a lot of examples to learn the important features of both languages and the patterns that allow mapping between them. 

Self-supervised and unsupervised machine learning methods are also used. Language models are often pre-trained on a related task that does not require manual labelling (e.g. filling in artificially created gaps) as this helps the model learn the structure of a language before it has to translate it. Human languages can also be translated by mapping their word embedding matrices (where words with similar meanings cluster together) as these tend to have similar shapes.

## Cetacean communication
Whales and dolphins have complex social behaviours and produce complex sounds that they seem to use for communication. This makes them a good candidate for decoding.

Humpback whales sing songs that can be heard over large distances (tens of kilometers). Each population of whales has a different song and this song changes over time - sometimes gradually and sometimes suddenly. A change in the song is propagated between individuals and between populations. Their songs have a hierarchical structure with themes and units of sounds.

Sperm whales produce clicks that form recognisable patterns. They seem to use some of these to identify themselves when they meet other whales. Calves take one to two years to learn these patterns and in the meantime they appear to 'babbel' like human infants do before they have acquired a language. 

## Challenges of translating non-human languages with A.I.
There are several major challenges in working with non-human animal communication.

### The data sets are small
This is the biggest bottleneck. The latest human language models are trained on billions of words and there is nowhere near this amount of data in from the rest of the animal kingdom.

### Audio is harder for machines to parse
Another challenge is that unlike human languages, non-human animal communication does not have a written form and is therefore harder for a machine to parse since there are many more dimensions in feature space (text can be 'tokenized' into a sequence of words or letters whereas sounds have a continuous range of frequency and amplitude).

### Non-humans may not rely primarily on sound
Humans primarily communicate through spoken, written or sign languages but non-human animals may use other methods of communication that we are either unaware of or do not record. Examples include ear movements, dancing, scents, pheromones and facial expressions.

### Labelling non-human animal communication requires behavioural and physiological data
Meaning can be extracted from human languages as we have people who can translate them into other languages. This gives us a labelled data set which makes it possible to train neural networks using supervised learning (the network is given the answer to learn from). This is not the case for animal communication. In order to extract meaning from non-human animal sounds we have to observe and measure their behaviours and link these to their sounds. This means labour intensive work for experts and/or a lot more data collection. 

## Available resources
- Hugging Face has an open [library of transformer models][hugging-face-transformers] and many of these have been pre-trained.
- TensorFlow has a [tutorial on creating transformer models][tensorflow-transformer-tutorial] for language translation.
- The [GitHub pages of Earth Species Project][esp-github] incudes datasets on whales, dogs, bats, birds and macaques as well as open discussions and tutorials.

## References
- <div class="csl-entry">Andreas, J., Beguš, G., Bronstein, M. M., Diamant, R., Delaney, D., Gero, S., Goldwasser, S., Gruber, D. F., de Haas, S., Malkin, P., Payne, R., Petri, G., Rus, D., Sharma, P., Tchernov, D., Tønnesen, P., Torralba, A., Vogt, D., &#38; Wood, R. J. (2021). <i>Cetacean Translation Initiative: a roadmap to deciphering the communication of sperm whales</i>. http://arxiv.org/abs/2104.08614</div>
- <div class="csl-entry">Artetxe, M., Labaka, G., Agirre, E., &#38; Cho, K. (2017). Unsupervised Neural Machine Translation. <i>6th International Conference on Learning Representations, ICLR 2018 - Conference Track Proceedings</i>. https://doi.org/10.48550/arxiv.1710.11041</div>
- <div class="csl-entry">Vaswani, A., Shazeer, N., Parmar, N., Uszkoreit, J., Jones, L., Gomez, A. N., Kaiser, Ł., &#38; Polosukhin, I. (2017). Attention Is All You Need. <i>Advances in Neural Information Processing Systems</i>, <i>2017-December</i>, 5999–6009. https://doi.org/10.48550/arxiv.1706.03762</div>

[ai-misuse-pathogenic-dna]: https://open-research.gemmadanks.com/notes/ai-misuse-pathogenic-dna/
[ai-sentience]: https://open-research.gemmadanks.com/notes/recognising-ai-sentience/
[biosignatures]: https://open-research.gemmadanks.com/notes/exoplanet-biosignatures/
[ceti]: https://www.projectceti.org/
[choosing-research-topic]: https://open-research.gemmadanks.com/planning/choosing-research-topic/
[esp]: https://www.earthspecies.org/
[esp-github]: https://github.com/earthspecies/project
[elephant-voices]: https://www.elephantvoices.org/
[elephant-listening-project]: https://elephantlisteningproject.org/
[google-ai-transformer-blog]: https://ai.googleblog.com/2017/08/transformer-novel-neural-network.html
[hugging-face-transformers]: https://huggingface.co/docs/transformers/index
[technosignatures]: https://open-research.gemmadanks.com/notes/technosignatures/
[tensorflow-transformer-tutorial]: https://www.tensorflow.org/text/tutorials/transformer
