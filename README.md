# Human Activity Tracking and Classification in a Restaurant

## Project Overview
This project aims to monitor and analyze human activities of restaurant workers using advanced computer vision techniques. By employing YOLO (You Only Look Once) for person tracking and a combination of LSTM (Long Short-Term Memory) and CNN (Convolutional Neural Networks) for activity recognition, we can efficiently determine whether workers are actively engaged in their tasks.

## Table of Contents
- [1. Dataset Creation for YOLO Person Tracking](#1-dataset-creation-for-yolo-person-tracking)


## 1. Dataset Creation for YOLO Person Tracking

### Overview
To effectively track restaurant workers using YOLO, a custom dataset was created, consisting solely of annotated images that focus on detecting the presence of individuals in a restaurant environment, without specific scenarios.

  
   


https://github.com/user-attachments/assets/31d9aadb-05fd-447a-8d47-00aeac995ab0




https://github.com/user-attachments/assets/19831596-9182-4d46-8aa7-285e6a91309c







## 2. Dataset Creation for LSTM-CNN Activity Recognition

### Overview
To recognize various human activities, a separate dataset was created that captures the actions of restaurant workers in defined scenarios, allowing for the classification of activities performed by multiple individuals.

### Activity Labels
The following activities are defined for classification:
- **Working**: Engaged in productive tasks.
- **Sitting and Working**: In a seated position while performing work tasks.
- **Not Working**: Includes other activities such as:
  - Sleeping
  - Using the phone
  - Sitting and Talking
  - Eating food









## Acknowledgments
- [YOLO](https://pjreddie.com/darknet/yolo/) for object detection.
- [Keras](https://keras.io/) and [TensorFlow](https://www.tensorflow.org/) for deep learning frameworks.
