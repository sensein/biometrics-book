## Extracting Vocal Features

In Senselab, we have a number of ways to investigate vocal features such as jitter, shimmer, and harmonics-to-noise ratio (HNR).

Jitter is a measure of deviations between consecutive period lengths for the fundamental frequency, which is a measure of the average number of sound wave oscillations occurring per second. Pathological jitter values are too high, and indicate irregular vocal-fold closure and asymmetric vibrations. To listeners, voices with pathological jitter may be perceived as roughness or breathiness. Although Senselab offers a variety of methods of calculating jitter, for the examples generated below we used the Relative Average Perturbation jitter (rap jitter), which the feature extraction package Praat Parselmouth defines as “the average absolute difference between a period and the average of it and its two neighbours, divided by the average period.”

Shimmer is a measure of differences in the amplitudes of consecutive fundamental frequency waves. Vocal shimmer is described as pathological when the value is too high, and there are irregularities in voice intensity. Like jitter, differences in shimmer can be perceived as roughness or breathiness. Although Senselab offers a variety of ways to calculate jitter, for the examples generated below we used local shimmer in decibels, which Praat Parselmouth defines as “average absolute base-10 logarithm of the difference between the amplitudes of consecutive periods, multiplied by 20.”

Harmonics-to-noise ratio (HNR) is the ratio between the fundamental frequency and noise components of the audio sample. HNR is calculated using the ratio between the fundamental frequency ($f_0$) and noise components, with pathological values being lower than healthy values. It indirectly correlates with perceived aspiration; that is, it can make someone’s voice sound “wet”, like they are inhaling spit or their throat is a bit clogged. This may be due to reducing laryngeal muscle tension resulting in a more open, turbulent glottis.

### Examples

#### Pathological Voices
Here are some samples of pathological voices:

https://github.com/user-attachments/assets/f91a9a2e-2949-4f76-afff-81f517655d9a

jitter:  0.037900850606389244

shimmer: 1.676462834189108

HNR: 1.2947330281343084

https://github.com/user-attachments/assets/a5a83052-c494-4d95-9014-76926fa0fc2e

jitter: 0.03130158503405692

shimmer: 1.5723108236836139

HNR: -0.32469447069195984

https://github.com/user-attachments/assets/86f94672-5e3c-438d-a9dc-673fe91c65fd

jitter: 0.013677889353212663

shimmer: 1.4152395591244642

HNR: 2.275629577740566


#### Healthy Voices

Here are some samples of healthy voices:

Example #1:


https://github.com/user-attachments/assets/14fa5eca-bd2b-4e25-9592-2f0f5ba18f28


jitter: 0.0071867455223159965

shimmer:  0.9633706166993545

HNR:  10.510586830939234

Example #2:

https://github.com/user-attachments/assets/92f071b0-b349-4c5f-9efc-c9d805240344

jitter: 0.008777987344689339

shimmer:  1.2210499662185004

HNR:  5.982610075269276


#### Modified Heatlhy Voices
Next, we processed the healthy voice samples by overlaying white noise onto them. Here is how the jitter, shimmer, and HNR metrics changed:

Example Healthy Audio #1 Overlayed with White Noise:


https://github.com/user-attachments/assets/4f3ba5e1-f3c7-4ca9-a03b-e627313e464b

jitter: 0.00940760475331362

shimmer:  1.0540879142722108

HNR:  6.982661343704628

Example Healthy Audio #2 Overlayed with White Noise:


https://github.com/user-attachments/assets/a0d23ac3-7557-4209-b74b-8e8cecc58f4c


jitter: 0.00879798298124843

shimmer:  1.3029822671906663

HNR:  3.8271737749636183


### Summary
Here are some summary graphs for the different types of voices.
![jitter_distribution](https://github.com/user-attachments/assets/584a8ecd-b430-438b-8d04-87614d6c6676)
![shimmer_distribution](https://github.com/user-attachments/assets/0d0c5ef9-a32f-444b-a2b0-18fa2ea19406)
![hnr_distribution](https://github.com/user-attachments/assets/48df984b-a15c-4b23-8195-a43e15a712ca)

### Open Questions:
There are many different metrics for jitter, including Local Jitter, Local Absolute Jitter, and Rap Jitter. There are also many different metrics for shimmer, including Local Shimmer and Local dB Shimmer. We could not find any literature on the advantages of using certain metrics for jitter and shimmer as opposed to other ones.

The literature is conflicted on the thresholds for determining in a voice’s jitter, shimmer, and HNR values are pathological. Praat Parselmouth and Opensmile both reference the Multi-Dimensional Voice Project (MDVP), however the thresholds established by this project are not very consistent with our data. Moreover, we could determine a potential threshold value of HNR from any of the literature, because the number stated by most papers cited a paper that did not actually include that number. Because of this, determining the actual thresholds for diagnosing pathologies remains an open question.

## Sources:
Teixeira, João Paulo, Carla Oliveira, and Carla Lopes. “Vocal Acoustic Analysis – Jitter, Shimmer and HNR Parameters.” Procedia Technology, CENTERIS 2013 - Conference on ENTERprise Information Systems / ProjMAN 2013 - International Conference on Project MANagement/ HCIST 2013 - International Conference on Health and Social Care Information Systems and Technologies, 9 (January 1, 2013): 1112–22. https://doi.org/10.1016/j.protcy.2013.12.124.
Tylečková and Skarnitzl, “The Mapping of Voice Parameters in Connected Speech of Healthy Common Czech Male Speakers.”

Williamson, “Acoustic Measures (Norms).”

“3.10. Fundamental Frequency (F0) — Introduction to Speech Processing.”

“3.14. Jitter and Shimmer — Introduction to Speech Processing.”

“Acted Emotional Speech Dynamic Database - AESDD.”

“Biometrics Book Features Examples.”

“cPitchJitter — openSMILE Documentation.”

“Cut Your Video in the Browser.”

“Perplexity.”

“Sensein/Senselab: Senselab Is a Python Package That Simplifies Building Pipelines for Biometric (e.g. Speech, Voice, Video, Etc) Analysis.”

“White Noise | Royalty-Free Music.”
