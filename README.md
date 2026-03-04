# Soccer Highlights Generator using Inflated 3D CNN

An automated video summarization system that generates soccer match
highlights using deep learning. The system processes a full soccer match
video and extracts key events such as **goals, substitutions, and
cards**, producing a condensed highlight reel.

The model is built using an **Inflated 3D Convolutional Neural Network
(I3D)** architecture that captures both **spatial and temporal
features** from video frames to detect important match events.

------------------------------------------------------------------------

# Project Overview

Soccer matches are long and fans often prefer watching highlights
instead of full games. This project automatically identifies key moments
in a match and compiles them into a summarized highlight video.

The system performs the following steps:

1.  Processes full soccer match videos
2.  Detects important events using a trained deep learning model
3.  Extracts timestamps of detected events
4.  Generates a summarized highlight video

------------------------------------------------------------------------

# Model Performance

  Metric      Score
  ----------- ------------
  Precision   **96.44%**
  Recall      **97.14%**
  F1 Score    **96.88%**
  Accuracy    **96.4%**

------------------------------------------------------------------------

# Dataset

The model is trained using the **SoccerNet dataset**, a large-scale
soccer video dataset containing **500 full matches** across major
European leagues.

### Target Event Classes

-   Goal
-   Card
-   Substitution

------------------------------------------------------------------------

# Model Architecture

The system uses an **Inflated 3D Convolutional Neural Network (I3D)**
which extends traditional 2D CNNs into 3D to capture motion and temporal
information in video sequences.

Key architecture characteristics:

-   Input dimension: **224 × 224 × 3**
-   3D convolution layers
-   Max pooling layers
-   Batch normalization
-   ReLU activation
-   Two fully connected layers
-   Softmax output layer

------------------------------------------------------------------------

# Project Pipeline

## 1. Data Preprocessing

-   Extract labeled clips from full match videos
-   Capture frames **45 seconds before event timestamps**
-   Convert clips into model input format

## 2. Dataset Split

-   **85% Training**
-   **10% Validation**
-   **5% Testing**

------------------------------------------------------------------------

# Training

Training is performed using **Mini-Batch Stochastic Gradient Descent
(SGD)**.

  Parameter       Value
  --------------- -------
  Learning Rate   0.001
  Batch Size      6
  Momentum        0.9
  Weight Decay    1e-7

------------------------------------------------------------------------

# Results

Example test:

-   Input: **26‑minute soccer match**
-   Output: **3‑minute highlight video**

------------------------------------------------------------------------

# Future Improvements

-   CNN + LSTM hybrid models
-   Faster training methods
-   Expansion to other sports (cricket, tennis, baseball)

------------------------------------------------------------------------

# References

-   SoccerNet Dataset
-   Inflated 3D ConvNet (I3D)
-   Optical Flow based action recognition
