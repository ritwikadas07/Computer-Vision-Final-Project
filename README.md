# Sign Language Detection using LSTM and MediaPipe

## Acknowledgment
This project was developed by Ritwika Das (GWID: G30941802) and Aditi Vyas (GWID: G40802010) under the supervision of Professor Robert Pless for the course *Introduction to Computer Vision (CSCI 6527_10)* at George Washington University.

## Main Aim
Our aim is to transform the way we communicate with the deaf and hard of hearing community by developing a cutting-edge sign language detection system. By integrating Long Short-Term Memory (LSTM) networks with MediaPipe technology, our project is designed to precisely recognize and interpret sign language from live video inputs.

# Process Overview

## 1. We Imported and Installed Dependencies
We ensured that all necessary libraries and frameworks were installed, including TensorFlow, Keras, and MediaPipe, which facilitated the development of our models and the processing of video data.

## 2. We Extracted Keypoints using MediaPipe Holistic
We utilized MediaPipe Holistic to detect and extract keypoints from video frames. These keypoints were crucial for analyzing human gestures in sign language, allowing us to gather detailed spatial data on sign language movements.

## 3. We Built the Sign Language Detection Models
We developed deep neural networks using TensorFlow and Keras, incorporating LSTM layers. The LSTM layers were chosen for their optimal performance in sequence prediction, which is essential for handling the sequential data of keypoints derived from sign language gestures.

## 4. We Implemented Real-Time Sign Language Prediction
We successfully implemented models to predict sign language in real-time using video sequences. This process involved processing live video inputs, extracting keypoints, and using these keypoints in our LSTM networks to accurately classify sign language gestures.

## Learning Outcomes
Participants will gain hands-on experience in:
- Extracting keypoints for sign language recognition using MediaPipe Holistic.
- Constructing and training a deep learning model with LSTM layers suitable for action detection.
- Applying the model to predict sign language in real-time from video sequences.

# Running the Code

This section guides you through the steps necessary to set up and run the project code effectively.

## Step 1: Imported and Installed Dependencies
We began by installing all required dependencies to ensure our setup matched the project requirements. We used the following command to install them:

```bash
pip install tensorflow==2.18.0 opencv-python mediapipe scikit-learn matplotlib
```

## Step 2: Keypoints using MP Holistic
We utilized the MediaPipe framework to extract keypoints using the Holistic model. This involved initializing MediaPipe components and defining functions to process the video input and draw landmarks. This step was crucial for capturing the dynamic movements involved in sign language. Below is an example picture:

![Alt text](record_keypoint.png "Hello")

## Step 3: Extract Keypoint Values
We extracted keypoints from poses, faces, and hands. These keypoints were critical as they represented the coordinates necessary for the LSTM model to learn the sign language gestures. The keypoints were saved as numpy arrays for further processing.

## Step 4: Setup Folders for Collection
We organized our dataset by creating directories for each action our model needed to recognize. This structured approach helped us manage and access video data efficiently during training and testing.

## Step 5: Collect Keypoint Values for Training and Testing
Using our webcam, we captured video sequences. As we performed or displayed sign language gestures in front of the camera, the system extracted and stored keypoints from each video frame. These keypoints served as the training and testing data for our LSTM model. 

For each label, it collected 30 frames which were shown at the top-left corner of the window written as "Collecting frames from {label} Video Number: {number}". The labels were "Thanks", "Hello", and "I love you". For this, we clicked 15 frames with the right hand and the next 15 frames with the left hand. Below are the sample pictures taken:

![Alt text](data_hello.png "Hello")

![Alt text](data_thanks.png "Thanks")

![Alt text](data_iloveyou.png "I Love you")

## Step 6: Preprocess Data and Create Labels and Features
We prepared our data for the LSTM network by creating labels and organizing sequence data. This preprocessing step converted raw keypoints into a structured format that the neural network could understand and learn from.

## Step 7: Build and Train LSTM Neural Network
We constructed the LSTM model using TensorFlow and trained it with the collected data. This step involved defining the architecture of the LSTM network and tuning parameters to optimize performance.

## Step 8: Make Predictions
We used the trained model to make predictions on new video data to test the effectiveness of our sign language detection system. This allowed us to validate the model's accuracy and make necessary adjustments.

## Step 9: Evaluation
We evaluated the model's performance using metrics such as the confusion matrix and accuracy rate. This evaluation helped us identify strengths and weaknesses in the model's ability to recognize different sign language gestures.

## Step 10: Real-Time Testing
Finally, we tested the system in real-time with live video input from our webcam. This step was essential to see how the model performed in practical scenarios and provided insights into real-world application feasibility. Below are the example pictures taken during the real-time prediction:

![Alt text](real_hello.png "Hello")

![Alt text](real_thanks.png "Thanks")

![Alt text](real_iloveyou.png "I Love you")
