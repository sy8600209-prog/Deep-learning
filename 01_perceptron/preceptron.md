# 🧠 Perceptron: The Fundamental Building Block

Welcome to the **Perceptron** module. This folder covers the absolute foundation of deep learning. Inspired by the biological neuron, the perceptron is a mathematical model that takes multiple binary inputs, processes them using weights and a bias, and outputs a single binary classification.

## 📐 Mathematical Architecture

At its core, a perceptron acts as a linear classifier. The operation can be broken down into two main steps:

### 1. The Linear Combination
The perceptron computes the weighted sum of its inputs and adds a bias term. In vector notation, this is represented as:

$$z = \mathbf{w}^T \mathbf{x} + b$$

Where:
* $\mathbf{x}$ is the input feature vector $(x_1, x_2, ..., x_n)$
* $\mathbf{w}$ is the weight vector $(w_1, w_2, ..., w_n)$
* $b$ is the bias (which shifts the decision boundary)

### 2. The Activation Function
The resulting sum $z$ is then passed through an activation function to determine the final output. For a classic perceptron, we use a **Heaviside step function**:

$$\hat{y} = \begin{cases} 1 & \text{if } z \ge 0 \\ 0 & \text{if } z < 0 \end{cases}$$

## ⚙️ The Learning Rule

The perceptron learns by adjusting its weights based on the error of its predictions. If the prediction $\hat{y}$ is incorrect compared to the true label $y$, the weights and bias are updated using the learning rate $\eta$:

$$w_i \leftarrow w_i + \eta (y - \hat{y}) x_i$$
$$b \leftarrow b + \eta (y - \hat{y})$$

* If the prediction is correct ($y = \hat{y}$), the weights do not change.
* If the prediction is wrong, the weights are pushed in the direction that reduces the error.

## 🚧 Limitations (The XOR Problem)

While the perceptron is great for logically linearly separable problems (like AND / OR gates), it fundamentally fails when data cannot be separated by a single straight line (a hyperplane). 

The most famous example of this is the **XOR problem**. A single perceptron cannot learn the XOR logic gate. This limitation is exactly why we need non-linear activation functions and hidden layers—which leads directly into the next phase of this repository: **Artificial Neural Networks (ANN)**.

## 💻 What's in this Folder?
*(Update this section based on the exact files you create)*
* `perceptron.py`: Custom implementation of the perceptron from scratch.
* `logic_gates.ipynb`: Training the perceptron to learn basic AND/OR logic gates.
* `visualizations/`: Plots showing the linear decision boundary adjusting during training.
