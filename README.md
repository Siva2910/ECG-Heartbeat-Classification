# ECG-Heartbeat-Classification

# Abstract : 

Electrocardiogram(ECG) is a valuable clinical signal, which is widely used to identify cardiovascular diseases. However, it remains a cumbersome process to manually evaluate the ECG signals because of smaller variations in its physiological features in normal and abnormal cases that too when there are a huge number of cardiac patients to examine. In such a scenario, automatic classification of ECG signals can provide an ease to the doctors to make a correct diagnosis of a particular disease.


# Introduction : 

![image](https://user-images.githubusercontent.com/67836160/176492822-e96818a6-1e6c-43bf-9b5b-bf1b6ebfe3b0.png)


Basically Arrhythmia refers to an irregularity in the rate or rhythm of the heartbeat, that means beating too fast or too slow or  with an irregular rhythm.I  have used a classification model to classify the ECG into five different classes of Arrhythmia based on their morphological features. The model which i used to implement this  is 1D-CNN whose architecture is based on three convolutional, max pooling and dense layers which automatically extracts distinguishable nonlinear features from the ECG signals and automatically classify them into five different classes: Non-ectopic beats (Normal Beat), Supraventricular ectopic beats, Ventricular ectopic beats, Fusion Beats and Unknown Beats. 

# Dataset :

![train](https://user-images.githubusercontent.com/67836160/176492463-af0d2843-664a-4581-9615-34db1e0fccd0.png)


I am using an open-source database of MIT-BIH for the classification of heartbeat, which is based on 47 subjects.This dataset is a famous collection of heartbeat signals used in heartbeat classification. The number of samples in  this collection is large enough for training a deep neural network.
The signals correspond to electrocardiogram (ECG) shapes of heartbeats for the normal case and the cases affected by different arrhythmias and myocardial infarction. These signals are preprocessed and segmented, with each segment corresponding to a heartbeat.
The MIT-BIH Arrhythmia Database contains 48 half-hour excerpts of two-channel ambulatory ECG recordings which are  obtained from 47 subjects studied by the BIH Arrhythmia Laboratory between 1975 and 1979. Twenty-three recordings were chosen at random from a set of 4000 24-hour ambulatory ECG recordings collected from a mixed population of inpatients (about 60%) and outpatients (about 40%) at Boston’s Beth Israel Hospital; the remaining 25 recordings were selected from the same set to include less common but clinically significant arrhythmias that would not be well-represented in a small random sample . Basically the dataset contains two folders train and test.


Each sample in the train and test file has 187 input features and one column indicates classification labels.

Heartbeats in the dataset fall into 5 categories as below : 

0 - Non ectopic
1 - Supraventricular
2 - Ventricular
3 - Fusion beats
4 - Unknown Beats

The Dataset is very imbalance , i have balanced the dataset by resampling samples from the class with a lower count in order to match the count of the class with a higher count.

To do this i have separated the dataset into 5, each containing samples belong to a particular class , Then each one is been resampled to get 5000 samples each , then the five datasets are then concatenated to get  a balanced dataset with 250000 samples in total.

 ![spread](https://user-images.githubusercontent.com/67836160/176492553-3caaf4e1-9838-4156-a9d8-2c4d26344dc9.png)
 
 # Model Workflow
 
 ![workflow](https://user-images.githubusercontent.com/67836160/176492651-f5a50123-6ba0-4c2c-8222-4e5df8301257.png)
 
 # Results :
 
 ![image](https://user-images.githubusercontent.com/67836160/176492749-2d54b6f8-07f2-4ada-ad46-5cf1b89472c3.png)


