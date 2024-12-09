# Sign Language Detection using LSTM and MediaPipe

## Acknowledgment
This project was developed by Ritwika Das (GWID: G30941802) and Aditi Vyas (GWID: G40802010) under the supervision of Professor Robert Pless for the course *Introduction to Computer Vision (CSCI 6527_10)* at George Washington University.

## Main Aim
The primary goal of this project is to create a sign language detection system that employs Long Short-Term Memory (LSTM) networks and MediaPipe technology. This system is designed to accurately recognize sign language from video inputs, providing an effective communication tool for the deaf and hard of hearing community.

## Process Overview

### 1. Import and Install Dependencies
Ensure all necessary libraries and frameworks are installed, including TensorFlow, Keras, and MediaPipe, to facilitate model development and video processing.

### 2. Extract Keypoints using MediaPipe Holistic
Use MediaPipe Holistic to detect and extract keypoints from video frames, which are crucial for analyzing human gestures in sign language.

### 3. Build the Sign Language Detection Model
Develop a deep neural network using TensorFlow and Keras, incorporating LSTM layers. LSTMs are optimal for sequence prediction, making them effective for handling the sequential data of keypoints derived from sign language.

### 4. Real-Time Sign Language Prediction
Implement the model to predict sign language in real time using video sequences. This step involves processing live video inputs, extracting keypoints, and using them in the LSTM network to classify sign language gestures.

## Learning Outcomes
Participants will gain hands-on experience in:
- Extracting keypoints for sign language recognition using MediaPipe Holistic.
- Constructing and training a deep learning model with LSTM layers suitable for action detection.
- Applying the model to predict sign language in real-time from video sequences.

# Running the Code

This section guides you through the steps necessary to set up and run the project code effectively.

## Step 1: Import and Install Dependencies
Begin by installing all required dependencies to ensure your setup matches the project requirements. Use the following command to install them:

```bash
pip install tensorflow==2.18.0 opencv-python mediapipe scikit-learn matplotlib
```

## Step 2: Keypoints using MP Holistic
Utilize the MediaPipe framework to extract keypoints using the Holistic model. This involves initializing MediaPipe components and defining functions to process the video input and draw landmarks. This step is crucial for capturing the dynamic movements involved in sign language.
Below is an example picture:
![Alt text](record_keypoint.png "Hello")

## Step 3: Extract Keypoint Values
Extract keypoints from poses, faces, and hands. These keypoints are critical as they represent the coordinates necessary for the LSTM model to learn the sign language gestures. The keypoints are saved as numpy arrays for further processing.

## Step 4: Setup Folders for Collection
Organize your dataset by creating directories for each action your model needs to recognize. This structured approach helps in managing and accessing video data efficiently during training and testing.

## Step 5: Collect Keypoint Values for Training and Testing
Use your webcam to capture video sequences. As you perform or display sign language gestures in front of the camera, the system extracts and stores keypoints from each video frame. These keypoints serve as the training and testing data for your LSTM model.
For each lab, it will collect 30 frames which will shown at the top-left corner of the window written as "Collecting frames from {label} Video Number: {number}". Here the labels are "Thanks", "hello" and "i love you". For this we had clicked 15 frames with right hand and the next 15 frames with left hand.
Below are the sample pictures taken:
![Alt text](data_hello.png "Hello")

![Alt text](data_thanks.png "Thanks")

![Alt text](data_iloveyou.png "I Love you")

## Step 6: Preprocess Data and Create Labels and Features
Prepare your data for the LSTM network by creating labels and organizing sequence data. This preprocessing step converts raw keypoints into a structured format that the neural network can understand and learn from.

## Step 7: Build and Train LSTM Neural Network
Construct the LSTM model using TensorFlow and train it with the collected data. This step involves defining the architecture of the LSTM network and tuning parameters to optimize performance.

## Step 8: Make Predictions
Use the trained model to make predictions on new video data to test the effectiveness of your sign language detection system. This allows you to validate the model's accuracy and make adjustments if necessary.

## Step 9: Evaluation
Evaluate the model's performance using metrics such as the confusion matrix and accuracy rate. This evaluation helps identify strengths and weaknesses in the model's ability to recognize different sign language gestures.

## Step 10: Real-Time Testing
Finally, test the system in real-time with live video input from your webcam. This step is essential to see how the model performs in practical scenarios and provides insights into real-world application feasibility.
Below are the example pictures taken during the real time prediction:
![Alt text](real_hello.png "Hello")

![Alt text](real_thanks.png "Thanks")

![Alt text](real_iloveyou.png "I Love you")
