# StateFarmDistractedDriverDetection


# Introduction

This project is about classification of the driver based on his/her position in the car.

# Dataset 

The dataset used in this project was provided by State Farm through a Kaggle competition, which is a set of images of
drivers taken inside a car capturing their activities such as texting, talking on the phone, eating, reaching behind, putting
on makeup, etc. As shown in Figure 1. These activities are classified into 10 classes as:
• c0: safe driving
• c1: texting — right
• c2: talking on the phone — right
• c3: texting — left
• c4: talking on the phone — left
• c5: operating the radio
• c6: drinking
• c7: reaching behind
• c8: hair and makeup
• c9: talking to a passenger

## Exploratory Visualization

![image](https://user-images.githubusercontent.com/101316217/211268395-34e6d7af-75f5-4e59-a192-9b2ef66f69dc.png)


## Data Exploration

There is one characteristic about the input data that may need to be addressed. I
noticed that some categories have more images than the others as we can see
from the chart below.

![image](https://user-images.githubusercontent.com/101316217/211268535-397f7b76-e5a9-4d7f-860b-52174ab5e910.png)

# Data Preprocessing

These are the data preprocessing steps that positively impacted results and were
applied on the data:
1. Images are converted into 3 channels, RGB – This preprocessing is done so
models may use the 3 channels to learn features with the objective of improving
accuracy and log loss.
2. Images are resized to 224 x 224 – Resizing images makes it easier to load on
memory at the cost of losing some details.
3.The list of images are normalized and divided into a train set and validation set -
This division is important so that we could validate if our model is improving or not
when it is training.

## Base model

![image](https://user-images.githubusercontent.com/101316217/211268771-5187126d-9ee0-463f-a6b3-2f318336cbaa.png)

## Baseline CNN

![image](https://user-images.githubusercontent.com/101316217/211268986-f7f0604e-461d-4038-bd3b-a876360bd3b8.png)

![image](https://user-images.githubusercontent.com/101316217/211269053-50ccc0f4-c2a5-4015-86eb-9f11513aeed7.png)

## Prediction Samples

![image](https://user-images.githubusercontent.com/101316217/211269378-4ef42c1c-9dba-4446-9668-3e5d7573f524.png)


## Transfer Learning

Vgg16 network was used 

![image](https://user-images.githubusercontent.com/101316217/211269672-c42811f6-f0ba-4250-8510-9405bb80cb92.png)


## CNN Visualization 

![image](https://user-images.githubusercontent.com/101316217/211269537-6fb7b1bd-a312-43cf-a382-99d1bb2f3c1a.png)


![image](https://user-images.githubusercontent.com/101316217/211269812-10aa7c8c-0790-4747-a2c1-22af9035687f.png)

![image](https://user-images.githubusercontent.com/101316217/211269910-92dc5972-b021-4171-9f86-9946c141f6b2.png)

## HeatMap

![image](https://user-images.githubusercontent.com/101316217/211270006-fef34cb4-dce6-4fa9-a9c5-6590e597f2b9.png)


# Future Work 

Use different networks in the transfer learning part

Models hyperparameters tuning 


