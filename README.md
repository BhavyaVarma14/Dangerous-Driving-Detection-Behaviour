# Dangerous Driving Detection Behavior

This project tackles the development of a deep learning model that classifies driver actions from dashboard camera images. The goal is to identify behaviors like distracted driving or safe driving in real-time.

## Problem Statement

Given a dataset of 2D dashboard camera images, classify each driver's behavior. This includes detecting activities like texting, talking on the phone, applying makeup, or simply driving safely.

## Project Tasks

### Data Acquisition and Preprocessing
1. **Download the dataset from Kaggle (State Farm Distracted Driver Detection competition).**
2. **Preprocess the images:**
   - Split into training and validation sets.
   - Resize to a standard size (e.g., 224x224 pixels).
   - Normalize pixel values by dividing by 255 and subtracting the mean (0.5).

### Model Building and Training
1. **Implement a Convolutional Neural Network (CNN) architecture.**
2. **Train the model on the prepared dataset.**

### Model Evaluation and Improvement
1. **Test the model's performance on unseen data.**
2. **Explore techniques to further improve accuracy and robustness.**

## Dataset Description

- **Source:** Kaggle (State Farm Distracted Driver Detection competition)
- **Format:**
  - `imgs.zip`: Compressed folder containing all images (train/test).
  - `sample_submission.csv`: Sample submission file in the correct format.
  - `driver_imgs_list.csv`: Training images with corresponding driver ID and class ID.
- **Image resolution:** 640x480 pixels (color)
- **Classes:** 10
  - `c0`: Safe driving
  - `c1`: Texting (right hand)
  - `c2`: Talking on phone (right hand)
  - `c3`: Texting (left hand)
  - `c4`: Talking on phone (left hand)
  - `c5`: Operating the radio
  - `c6`: Drinking
  - `c7`: Reaching behind
  - `c8`: Hair and makeup
  - `c9`: Talking to passenger
- **Total images:** 102,150
  - **Training images:** 17,939
  - **Validation images:** 4,485
  - **Test images:** 79,726

## Model Architecture

Standard CNN architecture with:
- 4 convolutional layers
- 4 max pooling layers in between
- Increasing filters from 64 to 512 across convolutional layers
- Dropout layers for regularization
- Flattening layer before fully connected layers
- 2 fully connected layers
- Final layer with 10 nodes and softmax activation for classification
- ReLU activation function for all other layers
- Xavier initialization for weights

## Further Development

- Explore alternative CNN architectures (e.g., VGG16, ResNet)
- Experiment with hyperparameter tuning for performance optimization
- Consider transfer learning from pre-trained models
- Implement data augmentation techniques for increased robustness

## Contributions

This project welcomes contributions from anyone interested in improving the model's accuracy and exploring new detection capabilities.

Feel free to contribute!
