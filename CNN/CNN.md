# 🧠 Convolutional Neural Networks (CNN)

Welcome to the **Convolutional Neural Networks** module. While standard ANNs flatten data and lose spatial information, CNNs are explicitly designed to process grid-like topology, such as images. By using convolutional filters, these architectures can extract hierarchical features—from simple edges to complex shapes—while drastically reducing the number of learnable parameters.

## 📓 Notebooks in this Folder

This directory contains implementations for two classic computer vision benchmarks, stepping up in complexity:

### 1. Digits Classification (MNIST)
This notebook serves as the "Hello World" of computer vision. 
* **Dataset:** 28x28 pixel grayscale images of handwritten digits (0-9).
* **Objective:** Build a foundational CNN architecture to correctly identify the digits.
* **Key Learnings:** Processing single-channel (1D) spatial data, transitioning from convolutional layers to fully connected (dense) layers, and achieving high accuracy on a relatively simple dataset.

### 2. CIFAR-10 Object Classification
This notebook tackles a significantly more complex vision task.
* **Dataset:** 32x32 pixel RGB (color) images categorized into 10 distinct classes (e.g., airplanes, automobiles, birds, cats).
* **Objective:** Design a deeper CNN capable of extracting features from multi-channel (3D) inputs.
* **Key Learnings:** Handling RGB channels, implementing strategies to prevent overfitting (like Dropout and Data Augmentation), and dealing with higher computational complexity compared to grayscale images.

## 🏗️ Core Architecture & Math Concepts

In these notebooks, you will implement and utilize the following spatial operations:

* **Convolution Operation:** The core building block where a kernel (filter) slides over the input image to create a feature map, preserving spatial relationships.
* **Spatial Dimension Formula:** When calculating the output size $O$ of a convolutional layer given an input size $W$, kernel size $K$, padding $P$, and stride $S$:
  
  $$O = \frac{W - K + 2P}{S} + 1$$

* **Pooling Layers (Max / Average):** Downsampling operations that reduce the spatial dimensions of the feature maps, minimizing computational load and providing translation invariance.
* **Flattening:** Converting the final 2D/3D feature maps into a 1D vector so it can be passed into a standard dense network for the final classification.

## 🛠️ Tech Stack Utilized
* **PyTorch & Torchvision:** For building the CNN models, applying transformations, and loading the MNIST and CIFAR-10 datasets.
* **Matplotlib:** For visualizing the image datasets, feature maps, and plotting training/validation loss and accuracy curves.
