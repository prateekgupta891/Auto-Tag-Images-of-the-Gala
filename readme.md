# HackerEarth Prize Competition- Auto-Tag Images of the Gala

This is a challenge hosted on HackerEarth and last date of submission was 7th April 2020.
## Major Highlights

1) Basic Pytorch Image Classification Code
2) Data Augmentation and Visualization 
3) Data Exploration and finding the correct normalization parameters.
4) KFold Classification
5) Prediction on unlabelled data

**Please give it a star if you like it.**

## Description

### **Problem statement**

Galas are the biggest parties of the year. Hosting firms of these events are well aware that everyone from around the world has their eyes on these nights. It can be for inspiration or for critique. It takes months of meticulous planning and delegation to host these events.

One such firm has decided to take a data-driven approach for planning their gala nights going forward. Aesthetics and entertainment are the most crucial segments of these events. So, this firm has hired you to help them aggregate and classify all images. These images are published by attendees and the paparazzi on various social media channels and other sources. You are required to build an image auto-tagging model to classify these images into separate categories.
Data

This data set consists of the following two columns:

    Column Name 	Description
    Image 	Name of Image
    Class 	Category of Image ['Food', 'Attire', 'Decorationandsignage', 'misc']

### **Data description**
The data folder consists of two folders and two CSV files.

Folders

    train: Contains 5983 images for 4 classes ['Food', 'misc', 'Attire', 'Decorationandsignage']
    test: Contains 3219 images

CSV files

    train.csv: (5983 x 2)
    test.csv: (3219x1)

sample_submission

    Image,Class
    image0001.jpg,Food
    image0002.jpg,Attire
    image0003.jpg,Food
    image0004.jpg,misc
    image0005.jpg,Attire

### **Evaluation metric**

    score = 100 * f1_score ( actual_values, predicted_values, average = 'weighted' )

Note: To avoid any discrepancies in the scoring, ensure all the index column ('Image_File') values in the submitted file match the values in the provided **test.csv** file.

[Competition Link](https://www.hackerearth.com/challenges/competitive/hackerearth-deep-learning-challenge-auto-tag-images-gala/machine-learning/auto-tag-images-of-the-gala-9e47fb31/)

## My understanding of the competition

It is a simple classification problem with evaluation metric as f1_score. Pre-trained classification architectures like Resnet or EfficientNet will work fine, with suitable data augmentations and regularizations. Hoping for a simple solution as my first try.

## My approach

1) Check class distribution for class imbalance
2) Train Images Visualization 
3) Check image shape variations to set the resize values
4) Create folders for dataset
5) Normalization Parameter
6) Train DataLoader and its visualization to set optimum data augmentation parameters
7) Train for KFold Classification batch wise with SGD loss
8) Save the best checkpoints based on best-achieved validation score.
9) Predictions using all the models( from each fold ) based on mean probability for each class over all the folds.

## Files

1) [Ipynb notebook](https://github.com/prateekgupta891/Auto-Tag-Images-of-the-Gala/blob/master/HackerEarth_Gala_Classification.ipynb)
2) [Open Notebook in colab](https://colab.research.google.com/drive/1WnrQMkQRwlG47pNwBV8BrBaxphzMrN8J)
3) [Dataset zipped](https://drive.google.com/open?id=1uHPc9sJ8jrKRLBYSo5p4QdAf_Y7cMqLu)
4) [Dataset with Train folder created(unzipped)](https://drive.google.com/open?id=14V54iwCWYRxmuBgFXk-SwTvRfBRzDwVb)

## Contributions 

Any contributions to my approach, involving enhancement, typos etc. will be highly appreciated.

## Issues

Do raise issues in case of any doubts or problems which may arise while running the code. 
(folder location issues may arise, will recommend to give it a few tries before creating an issue.)
