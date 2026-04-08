# CNN-project

### Fruit Classification using CNN
## Overview

This project uses a Convolutional Neural Network (CNN) to classify different types of fruits using the Fruits-360 dataset. The model is trained on 100x100 images and can recognize multiple varieties of fruits with high accuracy.

## Dataset
Fruits-360 dataset (100x100 branch)
Total images: 180,079
Training: 135,071 images
Test: 45,008 images
Number of classes: 257 (fruits, vegetables, nuts, and seeds)
All images are 100x100 pixels with 3 color channels (RGB)

## Source:
https://www.kaggle.com/datasets/moltean/fruits/data

## Model Architecture

The CNN model consists of:
Input  (100x100x3)
 -> Conv2D(32) + ReLU + MaxPool    # Detect edges & colors
 -> Conv2D(64) + ReLU + MaxPool    # Detect shapes & textures
 -> Conv2D(128) + ReLU + MaxPool   # Detect fruit-level patterns
 -> Flatten
 -> Dense(128) + Dropout(0.5)
 -> Dense(NUM_CLASSES) + Softmax   # Output class probabilities

Optimizer: Adam
Loss: Categorical Crossentropy
Metrics: Accuracy

## Features
Training with EarlyStopping and ModelCheckpoint to prevent overfitting
Plots for accuracy and loss curves
Evaluation on test set to calculate final accuracy
Option to plot confusion matrix for detailed analysis

## Results
Test Accuracy: ~ 99.74%
Test Loss: ~ 0.0141
