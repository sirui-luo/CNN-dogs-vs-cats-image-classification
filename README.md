# Dogs vs. Cats: Binary Image Classification Using Convolutional Neural Networks (CNN)
<img width="1348" alt="image" src="https://github.com/user-attachments/assets/6afaeddf-5def-4d15-b118-c5440c94d16b" />


**Project Objective**:  

The objective is to develop deep learning models for binary image classification - whether an image contains cat or dog - using Convolutional Neural Networks (CNNs). The project aims to:
* Apply image preprocessing techniques to prepare raw image data for training
* Design CNN-based models and evaluate model performance on binary classification tasks

**Data Description**:  
The dataset used is from the Dogs vs. Cats Redux competition, consisting of high-resolution JPEG images of dogs and cats intended for binary image classification.

**Model Evaluation**:  
In order to compare performance across different models, prediction probability (of being labelled as 1) is generated on the test dataset. Then the result is assessed via Kaggle’s log loss evaluation metric.

**Model Choosing**:  
***1. ResNet + logistic regression***:  
ResNet is a deep CNN architecture that uses residual connections to enable efficient training of very deep networks and is widely used for transfer learning. Here, the ResNet extracts a deep feature vector, which is passed to the added logistic layer to produce binary class probabilities for classification.

<img width="749" alt="image" src="https://github.com/user-attachments/assets/eb37a4a4-d638-40e7-a86c-970712b02279" />

***2. ResNet + XGBoosting***:  
In this pipeline, ResNet serves as a fixed feature extractor, generating deep 2048-dimensional feature vectors. These features are then passed to an external XGBoost classifier, which captures nonlinear patterns and feature interactions more effectively than a single logistic layer, leading to improved performance on binary classification tasks.

<img width="730" alt="image" src="https://github.com/user-attachments/assets/f99d5628-1719-4993-bd10-6d16fe4187b4" />

***3. ConvNeXt + logistic regression***:  
ConvNeXt-Tiny is a modern CNN inspired by transformer design. In this pipeline, a pretrained ConvNeXt-Tiny model is fully fine-tuned for binary classification by replacing its original head. It processes 224×224 normalized images and outputs softmax-based probabilities for two classes.

Compared to ResNet: ConvNeXt uses GELU activation, LayerNorm, and 7×7 depthwise convolutions to enhance stability and expand the receptive field. With gradual downsampling, inverted bottlenecks, and modern training techniques like AdamW and cosine scheduling, ConvNeXt delivers significantly better generalization.

<img width="704" alt="image" src="https://github.com/user-attachments/assets/5c778331-5ecf-4c72-881b-389f8a8e1c9e" />



