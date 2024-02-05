# Facial Emotion Detection using Machine Learning

## Importing Libraries:

- **cv2:** OpenCV library for computer vision tasks.
- **keras:** Deep learning library for neural network models.
- **numpy:** Library for numerical operations.

## Loading Pre-trained Model:

- The project loads a pre-trained deep learning model for facial emotion recognition.
- The model is loaded from a JSON file (`facialemotionmodel.json`) containing the architecture.
- Weights are loaded from a file (`facialemotionmodel.h5`) containing the trained parameters.

## Face Cascade Classifier:

- Utilizes the Haar Cascade Classifier from OpenCV to detect faces in the webcam feed.
- The classifier is loaded using `cv2.CascadeClassifier`.

## Feature Extraction Function:

- The `extract_features` function preprocesses the input image by reshaping and normalizing pixel values to the range [0, 1].

## Webcam Initialization:

- `cv2.VideoCapture(0)` initializes the webcam for capturing live video.

## Emotion Labels:

- A dictionary (`labels`) is defined to map predicted emotion indices to human-readable emotion labels.

## Main Loop:

- The script enters a while loop to continuously capture video frames from the webcam.

## Face Detection:

- The Haar Cascade Classifier is used to detect faces in the current video frame.

## Emotion Prediction:

- For each detected face, the code extracts the face region, preprocesses it, and feeds it to the loaded pre-trained model for emotion prediction.
- The predicted emotion label is retrieved from the `labels` dictionary.

## Display Results:

- The original video frame is annotated with rectangles around detected faces and the predicted emotion labels.
- The annotated frame is displayed using `cv2.imshow`.

## Exiting the Program:

- The loop continues until the 'Esc' key (27 in ASCII) is pressed.
- The program cleans up resources and exits.

## Exception Handling:

- There's a try-except block to handle any errors that may occur during face detection.
