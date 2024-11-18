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

## Development for Model and Chatbot

1. Model Development

  - For model development, we used Jupyter Notebook for the coding platform and imported necessary libraries as shown below
    ![image](https://github.com/user-attachments/assets/ffdafc96-4e6d-4e41-bad0-915474381f96)

  - For this project, we dont use many library packages as previous projects.

  - To load our dataset in YAML format, we use this relative pathway for easiness when changing PC
    ![image](https://github.com/user-attachments/assets/ba1549fd-874e-4d45-b16f-ec937630fdc4)

  - After load dataset, we load the pretrained model from Ultralytics. Here we use the smallest model and latest model, Yolo11n.
    ![image](https://github.com/user-attachments/assets/40ca1730-ae8e-447b-b977-8b15cc62dbde)

  - Then, we proceed with training the model with our custom dataset. We set our parameter with 50 epochs, seed = 42, imgsz = 640 and with patience of 10.
    ![image](https://github.com/user-attachments/assets/04c4f923-9f87-4931-85df-291df9dce918)

  - After the model trained, we chose the best model by weights after 50 epoch. This best model located in "runs/detect/train42/weights/best.pt". You can find it there.
    ![image](https://github.com/user-attachments/assets/176d33e5-bc19-40ee-8465-93ab910941e2)

  - Here we can see model metrics and it appear the model passed the needed criteria.
    ![image](https://github.com/user-attachments/assets/f1488879-a2f9-4a8a-bbe0-672433db19cb)

  - Thus, we proceed with the prediction to the model whether it can classify correctly
    ![image](https://github.com/user-attachments/assets/79da35ff-b0d9-4b69-939f-d5de243c9dd6)
    ![image](https://github.com/user-attachments/assets/78c2ffac-b88b-4a21-8d43-9329d0501a73)
  - As we can see, this shows the model managed to correctly classify the images. 

    





    

