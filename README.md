# Dogs vs. Cats: Binary Image Classification Using Convolutional Neural Networks (CNN)
<img width="1348" alt="image" src="https://github.com/user-attachments/assets/6afaeddf-5def-4d15-b118-c5440c94d16b" />


## Project Objective
The objective is to develop deep learning models for binary image classification - whether an image contains cat or dog - using Convolutional Neural Networks (CNNs). The project aims to:
* Apply image preprocessing techniques to prepare raw image data for training
* Design CNN-based models and evaluate model performance on binary classification tasks
* Demonstrate practical application of deep learning in computer vision

## Data Description
The dataset used is from the Dogs vs. Cats Redux competition (Kaggle competition). It consists of high-resolution JPEG images of dogs and cats intended for binary image classification.
  
  ### 1) Data Structure
  The dataset includes two main ZIP archives:
  * train.zip: Contains 12,500 labeled images of dogs and 12,500 labeled images of cats. (filename format: dog.0.jpg, dog.1.jpg, ..., cat.0.jpg, cat.1.jpg, ...)
  * test.zip: Contains 12,500 unlabeled images for model evaluation. (filename format: 1.jpg, 2.jpg, ..., 12500.jpg)

  ### 2) Label
  Target Variable: Binary label 1 for dog and 0 for cat

## Project Method
In this Cat VS Dog image classification project, Convolutional Neural Networks (CNNs) is used for image binary classification to distinguish between dogs and cats. Built with deep learning frameworks like TensorFlow and Keras, it showcases techniques in image processing and applying CNNs to binary classification problems.

## Model Evaluation
In order to compare performance across different models, prediction probability (of being labelled as 1) is generated on the test dataset. Then the result is assessed via Kaggle’s log loss evaluation metric.

## Model Choosing
### 1. ResNet
ResNet is a deep CNN architecture that uses residual connections to enable efficient training of very deep networks and is widely used for transfer learning.

<img width="718" alt="image" src="https://github.com/user-attachments/assets/7fe7cc1d-b8c6-4866-b773-c36699d744c2" />

