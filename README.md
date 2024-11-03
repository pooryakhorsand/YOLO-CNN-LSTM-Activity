# Human Activity Tracking and Classification in a Restaurant

## Project Overview
This project aims to monitor and analyze human activities of restaurant workers using advanced computer vision techniques. By employing YOLO (You Only Look Once) for person tracking and a combination of LSTM (Long Short-Term Memory) and CNN (Convolutional Neural Networks) for activity recognition, we can efficiently determine whether workers are actively engaged in their tasks.

## Table of Contents
- [1. Dataset Creation for YOLO Person Tracking](#1-dataset-creation-for-yolo-person-tracking)
- [2. Dataset Creation for LSTM-CNN Activity Recognition](#2-dataset-creation-for-lstm-cnn-activity-recognition)
- [3. Results](#3-results)

## 1. Dataset Creation for YOLO Person Tracking

### Overview
To effectively track restaurant workers using YOLO, a custom dataset was created, consisting solely of annotated images that focus on detecting the presence of individuals in a restaurant environment, without specific scenarios.

  
   

https://github.com/user-attachments/assets/2996aa1c-6636-4792-a3e5-4ba74063b99b



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

### Classification Logic
In the dataset, we label the activities as follows:
- If a worker is **Working** or **Sitting and Working**, we assign them the label **"Working"**.
- All other activities (Sleeping, Using the phone, Sitting and Talking, Eating food) are labeled as **"Not Working"**.



https://github.com/user-attachments/assets/b645b127-285f-4436-a7ab-49d76277cf15



https://github.com/user-attachments/assets/7cb3d2e2-2bd6-4034-a0a9-2ef9a67a1749



https://github.com/user-attachments/assets/f59ae2fe-1c14-4b2c-98a2-81fcf8649083



## 3. Results

### YOLO Person Tracking Results:
- The YOLO model, after training on the person tracking dataset, is capable of detecting workers within the restaurant environment accurately. Discuss the precision and recall metrics that highlight the model's effectiveness in identifying individuals.

### LSTM-CNN Activity Recognition Results:
- The LSTM-CNN model, trained on the activity recognition dataset, accurately classifies the defined activities even when there are multiple workers present. Include metrics such as accuracy, F1 score, and confusion matrix to demonstrate the model's performance. Showcase sample predictions to illustrate the scenarios where the model excels and any areas needing improvement.

### Conclusion
This project combines powerful computer vision techniques to analyze human activities in a restaurant setting. The insights gained can help improve workflow efficiency and productivity for restaurant operations.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
- [YOLO](https://pjreddie.com/darknet/yolo/) for object detection.
- [Keras](https://keras.io/) and [TensorFlow](https://www.tensorflow.org/) for deep learning frameworks.
