# Capstone-5-Finale

## Description
This finale capstone project is a simple project involving Computer Vision combined together with a Chatbot to classify five vegetable classes using Yolo Model (its also my fifth time posting here).
For this project, the five vegetables that we chose were Cucumber, Capsicum, Carrot, Cauliflower, and Potato. As for the indicators that project work properly, based on Mean Average Precision (mAP) and its inference time per image. 
Mean Average Precision (mAP) : > 0.75
Inference Time (per Image) : < 100ms 

## Data Collection 

We have three main sources of collecting data (images), first is Kaggle Vegetable Image Dataset (https://www.kaggle.com/datasets/misrakahmed/vegetable-image-dataset), which provide the bulk of data for this project. Second, we supplemented the dataset with high resolution online images of vegetables that can offered more detailed features of the vegetable itsefl thus increasing its probality of greater accuracy. Lastly, we obtained the data (images) by going to Vegetable aisle at local supermarket and doing some hands on photography where this method allowed a greater control over image quality and position of vegetables. 

## Data Process

Satisfied with data collected, we proceed with processing the images into more suitable format for model to learn. For this part, we used Bounding Box for our vegetable detection and we annotated and labelled the images using Roboflow (https://roboflow.com/). We divided the dataset into 70% for training, 15% for validation and another 15% for testing. These are the process we done in the Roboflow:
1. Resizing the all images into 640 x 640 resolution
2. Augmentation : Rotate 90 degree with upside down.

This augmentation process increased the variety of training data and will help the model to generalize vegetable better.

After that, we exported the dataset in YAML format, ready to be use for our YOLO model. 

## 
