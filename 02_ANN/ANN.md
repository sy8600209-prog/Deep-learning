# 🧠 Artificial Neural Networks (ANN)

Welcome to the **Artificial Neural Networks** module. Moving beyond the limitations of the single perceptron, this folder explores Multi-Layer Perceptrons (MLPs). By stacking layers of neurons and applying non-linear activation functions, ANNs can learn intricate patterns and solve complex, non-linearly separable problems.

## 📓 Notebooks in this Folder

This directory contains practical, hands-on implementations divided into the two foundational machine learning tasks:

### 1. Classification Notebook
This notebook focuses on categorizing data into distinct classes (binary or multi-class).
* **Core Concepts:** Cross-Entropy Loss, Sigmoid and Softmax activation functions.
* **Workflow:** Data preprocessing, forward propagation to generate class probabilities, and evaluating model metrics like accuracy and precision.

### 2. Regression Notebook
This notebook focuses on predicting continuous numerical values.
* **Core Concepts:** Mean Squared Error (MSE) loss, linear output layers without activation restrictions.
* **Workflow:** Feature scaling (e.g., using `StandardScaler`), training the network to minimize the distance between predicted and actual continuous values, and analyzing the loss curve.

## 🏗️ Core Architecture & Math Concepts

To understand the code in these notebooks, you will see the following concepts in action:

* **Hidden Layers:** The intermediate layers between the input and output that extract hidden features from the data.
* **Forward Pass:** The process of passing inputs through the network: `Output = Activation(Weights * Input + Bias)`.
* **Activation Functions:** Functions like ReLU (Rectified Linear Unit) and Tanh that introduce non-linearity, allowing the network to approximate complex functions.
* **Backpropagation:** The engine of deep learning. It calculates the gradient of the loss function with respect to each weight using the chain rule, passing errors backward through the network.
* **Optimizers:** Algorithms like Stochastic Gradient Descent (SGD) or Adam that update the weights to minimize the loss.

## 🛠️ Tech Stack Utilized
* **PyTorch:** For building, training, and optimizing the dense network architectures.
* **scikit-learn:** For data preprocessing, feature scaling, and dataset splitting.
* **Matplotlib / Plotly:** For visualizing training loss over epochs and plotting predictions.
