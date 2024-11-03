# Human Activity Tracking and Classification in a Restaurant

## Project Overview
This project aims to monitor and analyze human activities of restaurant workers using advanced computer vision techniques. By employing YOLO (You Only Look Once) for person tracking and a combination of LSTM (Long Short-Term Memory) and CNN (Convolutional Neural Networks) for activity recognition, we can efficiently determine whether workers are actively engaged in their tasks.

## Table of Contents
- [1. Dataset Creation for YOLO Person Tracking](#1-dataset-creation-for-yolo-person-tracking)
- [2. Dataset Creation for LSTM-CNN Activity Recognition](#2-dataset-creation-for-lstm-cnn-activity-recognition)
- [3. Results](#3-results)

## 1. Dataset Creation for YOLO Person Tracking

### Overview
To effectively track restaurant workers using YOLO, a custom dataset was created, consisting of annotated images and videos that capture various scenarios in a restaurant environment.

### Steps for Dataset Creation:
1. **Data Collection**: Gather images and videos of restaurant workers in various situations, such as serving food, taking orders, cleaning tables, etc. Ensure the dataset includes a diverse range of scenarios, angles, and lighting conditions.

2. **Annotation**:
   - Use annotation tools (e.g., LabelImg, VGG Image Annotator) to label the images. The annotations should include bounding boxes around each person, categorized as ‘worker’ or ‘non-worker’.
   - Save annotations in the YOLO format (a text file for each image that includes the class label and coordinates of the bounding boxes).

3. **Data Augmentation**:
   - To enhance the dataset, apply data augmentation techniques such as flipping, rotation, cropping, and color adjustments. This helps improve the model's robustness against overfitting.

4. **Dataset Split**: 
   - Split the dataset into training, validation, and test sets (typically 70% training, 15% validation, 15% testing).

## 2. Dataset Creation for LSTM-CNN Activity Recognition

### Overview
For recognizing different human activities, a second dataset was created that incorporates temporal dynamics via video frames.

### Steps for Dataset Creation:
1. **Data Collection**: Similar to the YOLO dataset but with a focus on capturing sequences of activities. Record videos of various activities performed by workers, such as cooking, serving, cleaning, and interacting with customers.

2. **Frame Extraction**:
   - From each recorded video, extract frames at a consistent rate (e.g., every 5 or 10 frames). Label each frame with the corresponding activity.

3. **Annotation**:
   - Annotate activity labels for each sequence of frames to indicate which activity is being performed. Ensure that each group of frames corresponds to a specific human activity.

4. **Data Preparation**:
   - Preprocess the images to a uniform size and normalize pixel values. Create sequences of frames to input into the LSTM-CNN model, organizing the data into an appropriate format (e.g., input shape of `[samples, time steps, height, width, channels]`).

5. **Dataset Split**: As with the YOLO dataset, split this dataset into training, validation, and testing sets.

## 3. Results

### YOLO Person Tracking Results:
- After training the YOLO model, it successfully detects workers in various scenarios within the restaurant environment. The precision and recall metrics for worker detection can be summarized here, showcasing the performance of the model.

### LSTM-CNN Activity Recognition Results:
- Upon training the LSTM-CNN model, it demonstrated accurate classification of the defined activities. Present various metrics (such as accuracy, F1 score, confusion matrix) to illustrate the model's performance. Include sample predictions to highlight scenarios where the model performs well and any challenging cases.

### Conclusion
This project combines powerful techniques in computer vision to analyze human activity in a restaurant setting. The insights gained from this analysis can be invaluable for improving efficiency and productivity in restaurant operations.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
- [YOLO](https://pjreddie.com/darknet/yolo/) for object detection.
- [Keras](https://keras.io/) and [TensorFlow](https://www.tensorflow.org/) for deep learning frameworks.
