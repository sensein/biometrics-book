## Extracting Vocal Features

In Senselab, we have a number of ways to investigate vocal features such as jitter, shimmer, and harmonics-to-noise ratio (HNR).

Jitter is a measure of deviations between consecutive period lengths for the fundamental frequency, which is a measure of the average number of sound wave oscillations occurring per second. Pathological jitter values are too high, and indicate irregular vocal-fold closure and asymmetric vibrations. To listeners, voices with pathological jitter may be perceived as roughness or breathiness. Although Senselab offers a variety of methods of calculating jitter, for the examples generated below we used the Relative Average Perturbation jitter (rap jitter), which praat parselmouth defines as “the average absolute difference between a period and the average of it and its two neighbours, divided by the average period.”

Shimmer is a measure of differences in the amplitudes of consecutive fundamental frequency waves. Vocal shimmer is described as pathological when the value is too high, and there are irregularities in voice intensity. Like jitter, differences in shimmer can be perceived as roughness or breathiness. Although Senselab offers a variety of ways to calculate jitter, for the examples generated below we used local shimmer in decibels, which praat parselmouth defines as “average absolute base-10 logarithm of the difference between the amplitudes of consecutive periods, multiplied by 20.”

Harmonics-to-noise ratio (HNR) is the ratio between the fundamental frequency and noise components of the audio sample. HNR is calculated using the ratio between the fundamental frequency ($f_0$) and noise components, with pathological values being lower than healthy values. It indirectly correlates with perceived aspiration; that is, it can make someone’s voice sound “wet”, like they are inhaling spit or their throat is a bit clogged. This may be due to reducing laryngeal muscle tension resulting in a more open, turbulent glottis.

### Examples

#### Pathological Voices
Here are some samples of pathological voices:

*INSERT breathiness.wav CLIP HERE*

jitter:  0.037900850606389244

shimmer: 1.676462834189108

HNR: 1.2947330281343084

*INSERT creakiness.wav CLIP HERE*
jitter: 0.03130158503405692

shimmer: 1.5723108236836139

HNR: -0.32469447069195984


*INSERT hoarseness.wav CLIP HERE*
jitter: 0.013677889353212663

shimmer: 1.4152395591244642

HNR: 2.275629577740566


#### Healthy Voices

Here are some samples of healthy voices:
Raw_audio_1:
*INSERT AUDIO CLIP HERE*
jitter: 0.0071867455223159965

shimmer:  0.9633706166993545

hnr:  10.510586830939234


Raw_audio_2:
*INSERT AUDIO CLIP HERE*
jitter: 0.008777987344689339

shimmer:  1.2210499662185004

hnr:  5.982610075269276


#### Modified Heatlhy Voices
Next, we processed the healthy voice samples by overlaying white noise onto them. Here is how the jitter, shimmer, and hnr metrics changed:

Raw Audio 1 Overlayed with White Noise:
*INSERT h1_white.mp4 AUDIO HERE!*

jitter: 0.00940760475331362

shimmer:  1.0540879142722108

hnr:  6.982661343704628

Raw Audio 2 Overlayed with White Noise:
jitter: 0.00879798298124843

shimmer:  1.3029822671906663

hnr:  3.8271737749636183


#### Summary
Here are some summary graphs for the different types of voices. *PLEASE ADD GRAPHS HERE*

# Open Questions:
There are many different metrics for jitter, including Local Jitter, Local Absolute Jitter, and Rap Jitter. There are also many different metrics for shimmer, including Local Shimmer and Local dB Shimmer. We could not find any literature on the advantages of using certain metrics for jitter and shimmer as opposed to other ones.
The literature is conflicted on the thresholds for determining in a voice’s jitter, shimmer, and HNR values are pathological. Praat Parselmouth and Opensmile both reference the Multi-Dimensional Voice Project (MDVP), however the thresholds established by this project are not very consistent with our data. Moreover, we could determine a potential threshold value of HNR from any of the literature, because the number cited by most papers referenced a paper that did not actually include that number. Because of this, determining the actual thresholds for diagnosing pathologies remains an open question.

## Sources:
Teixeira, João Paulo, Carla Oliveira, and Carla Lopes. “Vocal Acoustic Analysis – Jitter, Shimmer and HNR Parameters.” Procedia Technology, CENTERIS 2013 - Conference on ENTERprise Information Systems / ProjMAN 2013 - International Conference on Project MANagement/ HCIST 2013 - International Conference on Health and Social Care Information Systems and Technologies, 9 (January 1, 2013): 1112–22. https://doi.org/10.1016/j.protcy.2013.12.124.
Tylečková and Skarnitzl, “The Mapping of Voice Parameters in Connected Speech of Healthy Common Czech Male Speakers.”

Williamson, “Acoustic Measures (Norms).”

“3.10. Fundamental Frequency (F0) — Introduction to Speech Processing.”

“3.14. Jitter and Shimmer — Introduction to Speech Processing.”

“Acted Emotional Speech Dynamic Database - AESDD.”

“Biometrics Book Features Examples.”

“cPitchJitter — openSMILE Documentation.”

“Perplexity.”

“Sensein/Senselab: Senselab Is a Python Package That Simplifies Building Pipelines for Biometric (e.g. Speech, Voice, Video, Etc) Analysis.”

“White Noise | Royalty-Free Music.”
