<div align="center">

# 🧠 CNN Architectures & Transfer Learning

### Exploring Convolutional Neural Networks for Computer Vision

<p>
  <b>AlexNet • GoogLeNet • VGG16 • VGG19 • ResNet152 • Transfer Learning</b>
</p>

<p>
  <img src="https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow&logoColor=white">
  <img src="https://img.shields.io/badge/Deep%20Learning-CNN-purple">
  <img src="https://img.shields.io/badge/Computer%20Vision-CNN-green">
  <img src="https://img.shields.io/badge/Transfer%20Learning-ResNet-red">
</p>

</div>

---

## 📌 About This Repository

This repository contains my learning implementations and experiments with **Convolutional Neural Network (CNN) architectures** using **TensorFlow and Keras**.

The main goal of this repository is to understand how different CNN architectures work, how they evolved, and how pre-trained CNN models can be used for **Transfer Learning**.

The architectures covered in this repository include:

- **AlexNet**
- **GoogLeNet**
- **VGG16**
- **VGG19**
- **ResNet152**
- **ResNet Transfer Learning**
- **Rock-Paper-Scissors Image Classification**

This repository focuses on understanding the concepts behind CNNs rather than simply using pre-built models.

---

## 🎯 Objectives

The main objectives of this repository are:

- Understand the fundamentals of Convolutional Neural Networks.
- Learn how convolution layers extract features from images.
- Understand filters, kernels, padding, and stride.
- Understand pooling and feature-map generation.
- Study different famous CNN architectures.
- Understand the evolution of CNN architectures.
- Learn how pre-trained models work.
- Understand ImageNet pre-trained weights.
- Learn the concept of Transfer Learning.
- Apply a pre-trained ResNet model to a custom dataset.
- Understand image classification using deep learning.

---

## 🧠 CNN Architectures Covered

| Architecture | Main Concept |
|---|---|
| **AlexNet** | Deep CNN, ReLU and Dropout |
| **GoogLeNet** | Inception Modules |
| **VGG16** | Small 3×3 Convolution Filters |
| **VGG19** | Deeper VGG Architecture |
| **ResNet152** | Residual Learning and Skip Connections |
| **ResNet Transfer Learning** | Pre-trained Model + Custom Dataset |

---

# 🏗️ Architectures

## 1. AlexNet

**AlexNet** is one of the most influential CNN architectures in the development of modern Computer Vision.

It demonstrated the effectiveness of deep convolutional neural networks for large-scale image classification.

### Key Concepts

- Convolutional Layers
- ReLU Activation
- Max Pooling
- Fully Connected Layers
- Dropout
- Softmax Classification

### Basic Architecture

```text
Input Image
     ↓
Convolution
     ↓
ReLU
     ↓
Max Pooling
     ↓
Convolution
     ↓
ReLU
     ↓
Max Pooling
     ↓
Fully Connected Layers
     ↓
Softmax
     ↓
Predictionl
```


### Implementation

The AlexNet implementation in this repository focuses on understanding the architecture and its main components using TensorFlow/Keras.

---

## 2. VGG_16 and VGG_19



**VGG16** was introduced in the research paper *"Very Deep Convolutional Networks for Large-Scale Image Recognition"* by the Visual Geometry Group (VGG) at the University of Oxford.

The main idea behind VGG was to increase the depth of the network while using small **3×3 convolution filters**.

### 🔑 Key Concepts

- 3×3 Convolution Filters
- ReLU Activation
- Max Pooling
- Deep CNN Architecture
- Fully Connected Layers
- ImageNet
- Pre-trained Weights
- Feature Extraction
- Image Classification

```text
                 VGG Family
                     │
          ┌──────────┴──────────┐
          ↓                     ↓
       VGG16                  VGG19
          │                     │
     16 layers              19 layers
          │                     │
          └──────────┬──────────┘
                     ↓
              3×3 Convolutions
                     ↓
               Feature Learning
                     ↓
              Image Classification
```

## 3. GoogLeNet

**GoogLeNet**, also known as **Inception**, introduced the concept of the **Inception Module**, which allows the network to perform different types of operations in parallel.

### Key Concepts

- Inception Module
- 1×1 Convolution
- 3×3 Convolution
- 5×5 Convolution
- Max Pooling
- Feature Concatenation
- Computational Efficiency

### Basic Architecture

```text
Input Image
     ↓
Initial Convolution
     ↓
Pooling
     ↓
Inception Modules
     ↓
More Inception Modules
     ↓
Global Average Pooling
     ↓
Fully Connected Layer
     ↓
Softmax
     ↓
Prediction
```
## 4. ResNet152 — 2015

ResNet, or Residual Network, introduced the concept of Residual
Learning and Skip Connections.

The original ResNet paper was submitted in December 2015 and evaluated
networks up to 152 layers on ImageNet.

### 🔑 Key Concepts

- Residual Learning
- Skip Connections
- Residual Blocks
- Batch Normalization
- ReLU Activation
- Very Deep Networks
- ImageNet Pre-trained Weights

### Residual Block
```text
                 ┌──────────────────────┐
                 │                      │
                 │   Skip Connection    │
                 │                      │
Input ───────────┼──────────────────► (+) ──► ReLU
  │                                   ▲
  ↓                                   │
Conv → BatchNorm → ReLU → Conv ───────┘
```

### Inception Module

```text
                    ┌── 1×1 Convolution ──┐
                    │                     │
Input ──────────────┼── 3×3 Convolution ──┼──► Concatenate
                    │                     │
                    ├── 5×5 Convolution ──┤
                    │                     │
                    └── Max Pooling ──────┘
```

### ResNet152 Architecture

```text
Input Image
     ↓
Initial Convolution
     ↓
Max Pooling
     ↓
Residual Blocks
     ↓
Residual Blocks
     ↓
Residual Blocks
     ↓
Global Average Pooling
     ↓
Fully Connected Layer
     ↓
Prediction
```

The main idea is that the network learns a residual function rather than
having every layer learn the complete transformation directly. This made it
possible to train substantially deeper networks.

## 📜 CNN Architecture Timeline
```test
2012
 │
 └── AlexNet
       │
       ↓
2014
 │
 └── VGG16 / VGG19
       │
       ↓
2014
 │
 └── GoogLeNet / Inception
       │
       ↓
2015
 │
 └── ResNet
       │
       ↓
Practical Application
 │
 └── ResNet Transfer Learning
       │
       ↓
Rock-Paper-Scissors Classification
```

### 📊 Architecture Comparison
```
Year	        Architecture	                  Main Contribution
2012	        AlexNet	                          Deep CNN + ReLU + Dropout
2014	        VGG16 / VGG19	                  Deep networks with small 3×3 filters
2014	        GoogLeNet	                      Inception Modules + multi-scale processing
2015	        ResNet152	                      Residual Learning + Skip Connections
Practical Work	ResNet Transfer Learning	      Applying pre-trained knowledge to a custom dataset
```

### ⚙️ Technologies Used
<p align="center"> <img src="https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white"> <img src="https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow&logoColor=white"> <img src="https://img.shields.io/badge/Keras-red?logo=keras&logoColor=white"> <img src="https://img.shields.io/badge/NumPy-blue?logo=numpy&logoColor=white"> <img src="https://img.shields.io/badge/Matplotlib-green"> <img src="https://img.shields.io/badge/OpenCV-red?logo=opencv&logoColor=white"> </p>
Tools
Python
TensorFlow
Keras
NumPy
Matplotlib
OpenCV
Jupyter Notebook
Visual Studio Code