# Audio-Scene-Analysis-UrbanSound8k


### Intro
Sound Classification is one of the most widely used applications in Audio Deep Learning. It involves learning to classify sounds and to predict the category of that sound.
This type of problem can be applied to many practical scenarios e.g. classifying music clips to identify the genre of the music, or classifying short utterances by a set of speakers
to identify the speaker based on the voice.

Just like classifying hand-written digits using the MNIST dataset is considered a ‘Hello World”-type problem for Computer Vision, we can think of this application as the introductory
problem for audio deep learning.

We start with sound files, convert them into spectrograms, input them into a CNN plus Linear Classifier model, and produce predictions about the class to which the sound belongs.

This dataset contains 8732 labeled sound excerpts (<=4s) of urban sounds from 10 classes: air_conditioner, car_horn, children_playing, dog_bark, drilling, enginge_idling, gun_shot
, jackhammer, siren, and street_music. The classes are drawn from the urban sound taxonomy.
All excerpts are taken from field recordings uploaded to [freesound](www.freesound.org)  
#### To be noted- I ran this notebook on Kaggle and used urbansound8k dataset. If you use it on colab or on jupyter, please download the dataset from kaggle first.







### To do:
We use the Urban Sound 8K dataset that consists of a corpus of ordinary sounds recorded from day-to-day city life. The sounds are taken from 10 classes such as
drilling, dogs barking, and sirens. Each sound sample is labeled with the class to which it belongs.

After downloading the dataset, we see that it consists of two parts:

Audio files in the ‘audio’ folder: It has 10 sub-folders named ‘fold1’ through ‘fold10’. Each sub-folder contains a number of ‘.wav’ audio samples eg. ‘fold1/103074–7–1–0.wav’
Metadata in the ‘metadata’ folder: It has a file ‘UrbanSound8K.csv’ that contains information about each audio sample in the dataset such as its filename, its class label, the
‘fold’ sub-folder location, and so on. The class label is a numeric Class ID from 0–9 for each of the 10 classes. eg. the number 0 means air conditioner, 1 is a car horn, and so on.





### Methodology
There are 3 basic methods to extract features from audio file :
* Using the mffcs data of the audio files
* Using a spectogram image of the audio and then converting the same to data points (As is done forimages). This is easily done using mel_spectogram function of Librosa
* Combining both features to build a better model. (Requires a lot of time to read and extract data).
I have chosen to use the second method.

The labels have been converted to categorical data for classification.

### CNN has been used as the primary layer to classify data.
