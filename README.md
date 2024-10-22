# Driver-Drowsiness-Detection


Introduction

This project is centered around creating a Driver Drowsiness Detection System that observes the driver's eye status through a webcam. The system is designed to alert the driver if signs of drowsiness are detected. To achieve this, we employ OpenCV for both image capture and preprocessing, and we utilize a Convolutional Neural Network (CNN) to determine if the driver’s eyes are 'Open' or 'Closed.' An alarm will activate when drowsiness is identified.

Project Overview

The drowsiness detection process follows these key steps:

Image Capture: A webcam captures images of the driver.
Face Detection: The system identifies the driver’s face and establishes a Region of Interest (ROI).
Eye Detection: The eyes are detected within the ROI and forwarded to the classifier for analysis.
Eye Classification: The classifier evaluates the state of the eyes, categorizing them as either open or closed.
Drowsiness Score Calculation: A score is generated to assess drowsiness based on how long the driver’s eyes are closed.
CNN Model
The architecture of the Convolutional Neural Network is composed of:

Convolutional Layers:

First layer: 32 nodes with a 3x3 kernel
Second layer: 32 nodes with a 3x3 kernel
Third layer: 64 nodes with a 3x3 kernel
Fully Connected Layers:

A dense layer containing 128 nodes
Output layer with 2 nodes utilizing Softmax activation for classification
Activation Functions:

ReLU is employed in all layers except for the output layer.
The output layer uses Softmax to categorize the eye states as 'Open' or 'Closed.'
