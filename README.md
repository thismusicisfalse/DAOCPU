![](imagesStorage/Screenshot%202021-02-19%20at%204.51.00%20PM.png)

_DAOCPU_ is a composition that was informed by and developed in parallel to _Ensembl: An Ethereum-Based Platform for Decentralised Organising of Artistic Production_, which was initiated by Samson Young, Dr. Massimiliano Mollona, and MetaObjects (Andrew Crowe and Ashley Lee Wong) in 2020 (https://www.goethe.de/ins/gb/en/ver.cfm?fuseaction=events.detail&event_id=22087803).

At present, _DAOCPU_ is consisted of (1) a generative electronic composition written in CHUCK (https://chuck.cs.princeton.edu/); (2) a text visualization and analysis program written in Processing (https://processing.org/), which, is a standalone program but also has a "latent" relationship with the generative composition and may be played together; (3) drawings, which are inspired by the interactions that led to the development of _Ensembl_ (a sort of off-chain record of version history). Future components of _DAOCPU_ will include: musical instrument design, libretto, and costume. There are two categories of components: "generative" components, and "other" components. 

_DAOCPU_ encourages redistribution. The components within _DAOCPU_ may be listened to / viewed on their own. They may also be implemented as basis for recompositions and reperformance. While recomposition is always already possible, _DAOCPU_ includes more detailed documentation than what is usually available. _DAOCPU_ pays tribute to and contributes towards _Ensembl_, but is independent from it. It was inspired by, but also comments on, the evolving dynamics within _Ensembl_.

Technical documentations of the individual component are inside of each of the component's folder.

Below are more general, audience-facing descriptions of the currently-available components.

## Component 1: composition, _generative_

![](imagesStorage/Screenshot%202021-02-22%20at%2012.42.06%20PM.png)

This is a generative composition written in CHUCK. It is consisted of four sub-components: a conductor patch that controls time, and three sound-generating "musician" patches. 

By downloading the code, and also CHUCK's miniAudicle, a user may listen to / run the standalone version of the composition on the computer. In the standalone version, the musician patches (they are called 'Silvering,' 'Mum Changing Tempo,' and 'Blurred Roland') are making the sound, while the conductor is keeping track of when a patch is about to finish improvizing. When that happens, the conductor introduces the next patch in line, ensuring that there is enough of an overlap between patches so as not to break texture, but not so much that notes clash, or miniAudicle crash. The conductor ocassionally introduces samples of the heart mantra into the texture.

![](imagesStorage/Screenshot%202021-02-22%20at%2012.52.51%20PM.png)

The generative composition may also be paired with the visualization program. In this combination, the visualization program functions like a "meta-conductor". It generates "interruption melodies" that causes brief disruptions in musical time. The program achieves this by processing the text of the _Dao De Jing_, and translating punctuations into number of notes in a melody. It also takes over the introduction-of-mantra function from the conductor program.

## Component 2: Dao De Jing, _generative_

This is a text analysis program written in Processing. The program was mainly designed to perform analysis on a text, so that the results may be used to generate other non-text features (time for music, visual for costumes, 3d models, etc.). But it may also be viewed on its own.

The program takes a random chapter from James Legge's translation of the _Dao De Jing_ (https://en.wikipedia.org/wiki/Tao_Te_Ching) & (https://ctext.org/dao-de-jing), and filters the chapter using Daniel Howe's riTa library (https://rednoise.org/rita/#reference). At present, the program's filter leaves only the nouns and the punctuations in. The filtered text is the basis for timed-disruptions in the generative composition.

The program then performs phoneme analysis on the filtered text. Each phoneme is matched with a 3d-shape. These 3d-shapes were created using the "super shape" formula written by Paul Bourke (http://paulbourke.net/geometry/supershape/).


<img src="https://github.com/thismusicisfalse/DAOCPU/blob/main/imagesStorage/001.png" width="200"/>
<img src="https://github.com/thismusicisfalse/DAOCPU/blob/main/imagesStorage/002.png" width="200"/>

![](imagesStorage/Screenshot%202021-02-19%20at%204.49.16%20PM.png)

The program also performs additional sentiment analysis on the filtered text, using Google's Natural Language API (https://cloud.google.com/natural-language/). At present, this feature is provided, but is not linked to any non-text features.

