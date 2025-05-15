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
### 1. ResNet + logistic regression
ResNet is a deep CNN architecture that uses residual connections to enable efficient training of very deep networks and is widely used for transfer learning. Here, the ResNet extracts a deep feature vector, which is passed to the added logistic layer to produce binary class probabilities for classification.

<img width="749" alt="image" src="https://github.com/user-attachments/assets/eb37a4a4-d638-40e7-a86c-970712b02279" />


### 2. ResNet + XGBoosting
In this pipeline, ResNet serves as a fixed feature extractor, generating deep 2048-dimensional feature vectors. These features are then passed to an external XGBoost classifier, which captures nonlinear patterns and feature interactions more effectively than a single logistic layer, leading to improved performance on binary classification tasks.

<img width="777" alt="image" src="https://github.com/user-attachments/assets/9ab30190-040e-4697-9808-abb30e4d3343" />


### 3. ConvNeXt + logistic regression
ConvNeXt-Tiny is a modern CNN inspired by transformer design. In this pipeline, a pretrained ConvNeXt-Tiny model is fully fine-tuned for binary classification by replacing its original head. It processes 224×224 normalized images and outputs softmax-based probabilities for two classes.

Compared with ResNet: ConvNeXt modernizes the classic ResNet by incorporating design principles from Vision Transformers and lightweight CNNs. It replaces ReLU with smoother GELU activation, swaps BatchNorm for LayerNorm for better stability, and uses depthwise separable convolutions with larger 7×7 kernels to expand the receptive field. ConvNeXt applies a more gradual downsampling and inverted bottlenecks for richer feature extraction. Combined with modern training techniques like AdamW, cosine scheduling, and layer scaling, ConvNeXt achieves significantly better accuracy and generalization.

<img width="729" alt="image" src="https://github.com/user-attachments/assets/daa35db7-5707-4bc7-a45c-375bb8c57a8f" />


