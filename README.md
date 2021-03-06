# Environmental Sounds Automatic Classification
#### Rafela Machado and Victor Alves <br /> Centro Algoritmi, University of Minho, Braga, Portugal

> This project is the result of Rafaela Machado (rafapsm98@gmail.com) and Victor Alves (valves@di.uminho.pt) work, having been developed as part of Rafaela Machado's master thesis.

## Abstract

The study of ambient sounds suggests that human perception regarding the sound environment is influenced by the identification of sound sources. The assessment of ambient sounds reveals that they are made up of several sound sources and that human beings have an incredible capacity when it comes to their recognition.

The study of the relationship between the sound environment and the type of emotions aroused in human beings is, therefore, an important field to be studied since our brain interprets sound signals as sequences capable of creating systems of unprecedented meanings and of invoking images and feelings that may not be directly reflected from human memory.

The combination of the medical informatics branch with the study of ambient sounds results in thecreation of intelligent systems capable of not only identifying the sound sources, but also being able to distinguish the different types of emotions present in each distinct sound wave, which can, therefore lead to an improvement in health and well-being. Thus, the main part of this dissertation is to automatically classify sounds produced in the environment through Deep Learning techniques with the motivation to investigate and propose new solutions that improve the quality of life of the general population. This study is based on the exploration of the recognition of the sound source of ambient sound and on the subsequent classification of emotions that
are triggered from it at a psychological level in human beings.

Two different scenarios were then studied: in the first, ambient sounds classified according to their source were used, and from the extraction of their characteristics, an intelligent system was created capable of making the knowledge/identification of different sounds, in the second scenario, the information extracted in the first was used regarding the characteristics of the sound wave, creating clusters of sounds with similar characteristics and attributing to each one of them a type of emotion, later used as data for the creation of a second system, this time able to identify the feeling present in the sound wave.

In the end, the training results obtained suggest that it is possible to use Deep Learning techniques to improve the sound quality and consequently the well-being and health of the population.

## Materials and Methods

In this investigation, I used two datasets from which it became possible to create models capable of classifying sound as to its origin and emotional charge.

- [UrbanSound8K](https://urbansounddataset.weebly.com/urbansound8k.html)
- [FSD50K](https://annotator.freesound.org/fsd/release/FSD50K/)

##### Sound Pre-processing

It became important to extract some more characteristics of the wave using the Libro-sa library. Thus, data pre-processing consisted of extracting some characteristics: MFCC, SFTF, Honey-scaled power spectrogram, Octave-based spectral contrast and Tonnetz. These characteristics were then concatenated in vectors for each of the audios in the dataset. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/55671650/146695383-b2489682-b399-48c6-b2fa-9c003c5df73b.png" width="400" title="Audio pre-processing and feature extraction using the Librosa library">
</p>

##### Sound Classification

For the classification of sound different Machine Learning algorithms were used. An MLP model was used, a very simple network consisting of an input layer, a hidden layer and an output layer and an XGBoost algorithm combined with GridSearch, which allowed finding the parameters that best fit the type of data.
