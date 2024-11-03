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

### Steps for Dataset Creation:
1. **Data Collection**: Gather images of restaurant workers in various settings—focusing on different angles and lighting to ensure diversity. The key is to include a variety of worker poses and positions.

2. **Annotation**:
   - Utilize annotation tools (e.g., LabelImg, VGG Image Annotator) to label the images. The annotations should include bounding boxes around each worker.
   - Save annotations in the YOLO format (a text file for each image that includes the class label and coordinates of the bounding boxes).

3. **Data Augmentation**:
   - Enhance the dataset by applying data augmentation techniques such as flipping, rotation, cropping, and color adjustments to improve the model's performance.

4. **Dataset Split**: 
   - Split the dataset into training, validation, and test sets (typically 70% training, 15% validation, 15% testing).

## 2. Dataset Creation for LSTM-CNN Activity Recognition

### Overview
To recognize various human activities, a separate dataset was created that captures the actions of restaurant workers in defined scenarios, allowing for the classification of activities performed by multiple individuals.

### Steps for Dataset Creation:
1. **Data Collection**: Record videos capturing workers engaged in diverse activities within the restaurant, such as cooking, serving, cleaning, and interacting with customers.

2. **Frame Extraction**:
   - Extract frames from each video at a consistent interval (e.g., every 5 or 10 frames). Each extracted frame should be labeled with the corresponding activity being conducted during that time.

3. **Annotation**:
   - Annotate activity labels for sequences of frames to indicate which specific activity is being performed. Ensure that each group of frames corresponds to particular actions performed by the workers.

4. **Data Preparation**:
   - Preprocess images to a uniform size and normalize pixel values. Arrange the data into sequences suitable for input into the LSTM-CNN model, adhering to the desired input shape (e.g., `[samples, time steps, height, width, channels]`).

5. **Dataset Split**: Like the YOLO dataset, this dataset should be split into training, validation, and testing sets.

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
