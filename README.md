This project is a simple implementation of facial emotion detection using machine learning. Here's a breakdown of the code and its functionality:

1.Importing Libraries:
    cv2: OpenCV library for computer vision tasks.
    keras: Deep learning library for neural network models.
    numpy: Library for numerical operations.
    
2. Loading Pre-trained Model:
    It loads a pre-trained deep learning model for facial emotion recognition from a JSON file (facialemotionmodel.json) containing the model architecture and a        weights file (facialemotionmodel.h5) containing the trained weights.
   
3.Face Cascade Classifier:
    It uses the Haar Cascade Classifier from OpenCV to detect faces in the webcam feed. The classifier is loaded using cv2.CascadeClassifier.
    
4.Feature Extraction Function:
    The extract_features function is defined to preprocess the input image by reshaping it and normalizing pixel values to the range [0, 1].
  
5.Webcam Initialization:
    cv2.VideoCapture(0) initializes the webcam for capturing live video.
    
6.Emotion Labels:
    A dictionary labels is defined to map the predicted emotion index to human-readable emotion labels.
    
7.Main Loop:
    The script enters a while loop to continuously capture video frames from the webcam.
    
8.Face Detection:
    The Haar Cascade Classifier is used to detect faces in the current video frame.
    
9.Emotion Prediction:
    For each detected face, the code extracts the face region, preprocesses it, and feeds it to the loaded pre-trained model for emotion prediction. The predicted      emotion label is then retrieved from the labels dictionary.
    
10.Display Results:
    The original video frame is annotated with rectangles around detected faces and the predicted emotion labels. The annotated frame is displayed using cv2.imshow.
    
11.Exiting the Program:
    The loop continues until the 'Esc' key (27 in ASCII) is pressed. The program cleans up resources and exits.
    
12.Exception Handling:
    There's a try-except block to handle any errors that may occur during face detection.
