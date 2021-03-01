# Intel-Scene-Classification-Challenge

## Competition Link
https://datahack.analyticsvidhya.com/contest/practice-problem-intel-scene-classification-challe/

## Leaderboard Link
https://datahack.analyticsvidhya.com/contest/practice-problem-intel-scene-classification-challe/#LeaderBoard

## Problem Statement
How do we, humans, recognize a forest as a forest or a mountain as a mountain? We are very good at categorizing scenes based on the semantic representation and object affinity, but we know very little about the processing and encoding of natural scene categories in the human brain. In this practice problem, you are provided with a dataset of ~25k images from a wide range of natural scenes from all around the world. Your task is to identify which kind of scene can the image be categorized into.

## Dataset Description
There are 17034 images in train and 7301 images in test data. The categories of scenes and their corresponding labels in the dataset are as follows -

{'buildings' -> 0, 

'forest' -> 1,

'glacier' -> 2,

'mountain' -> 3,

'sea' -> 4,

'street' -> 5 }
 
There are three files provided to you, viz train.zip, test.csv and sample_submission.csv which have the following structure.

Variable	| Definition
|---|---|
image_name	| Name of the image in the dataset (ID column)
label	| Category of natural scene (target column)


train.zip contains the images corresponding to both train and test set along with the true labels for train set images in train.csv
 

## Evaluation Metric
The Evaluation metric for this competition is accuracy.

## Public and Private Split
Public leaderboard is based on randomly selected 30% of the test images, while private leaderboard will be evaluated on remaining 70% of the test images.

## Rank 25 Solution description
#### Public Leader Board Score: 0.961187214611872 Private Leader Board Score: 0.948933672471141

The solution uses simple averaging of 5 convnet models. The models were trained using transfer learning and progressive image resizing with the help of FastAI DL framework. Once cycle learning and learning rate tuning was also done. Below are the models that were tuned for the problem:

 1) resnet50, seed=2019
 2) resnet50, seed=35
 3) Densenet, seed = 2000
 4) Densenet, seed = 8888
 5) resnet101, seed = 123456

The notebook submission_2.ipynb contains the entire code.



