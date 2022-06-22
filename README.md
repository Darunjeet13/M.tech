# M.tech

Modern development in science and technology enables human to control device usingtheir brain. 
Brain Computer Interface (BCI) is a system where human brain communicate with a computer using brain signals. 
BCI system using Electroencephalogram (EEG) is a non-invasive method which uses brain signal to control robots. 
Brain control robots can assist people with disabilities to improve their livelihood.
We aims to control a robotic wheelchair using brain signal. 
To control wheelchair movement for rehabilitation using EEG, at first electrodes are placed on the subject’s scalp to acquire signal activity within brain. 
There are also devices available in market which can record brain signal. 
After that the signals got filtered using Fast Fourier Transformation (FFT) method to remove unwanted signal called artifacts. 
After that, to get useful features from that signal Power Spectral Density (PSD) method is used. 
To calculate PSD, welch method is used. Then Random forest classifier is used for classification of the wheelchair movement. 
For this purpose, a publicly available dataset from Kaggle is used (Link - https://www.kaggle.com/datasets/fabriciotorquato/eeg-data-from-hands-movement).
we have achieve a good accuracy.

We have first divided users data based on their movement , namely 0 ,1 and 2. This only contains dataset for user a.

To run this project follow below procedure.
Run eeg_psd_a.ipynb to extract features from EEG signal of user ‘a’. Those features are
saved in a csv file for later use. Then nun eeg_radom_forrest-psd.ipynb file to classify different movements of the user usingRandom forrest classification algorithm.
Run eeg_lgbm-psd.ipynb to classify the data using LGBM classification algorithm.
It also shows accuracy and confusion matrix for that user.
