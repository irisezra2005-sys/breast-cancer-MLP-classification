## Neural Network Architecture Report

# Breast Cancer Classification using Multi-Layer Perceptron (MLP)

# 1. Introduction

This project implements a Multi-Layer Perceptron (MLP) Neural Network for breast cancer classification. The objective of the model is to classify tumor samples into two categories: malignant and benign.

The MLP model consists of multiple fully connected layers that learn complex patterns from the input features. The network uses activation functions to introduce non-linearity, backpropagation to update weights, and an optimization algorithm to minimize the prediction error.


# 2. Neural Network Architecture

The implemented MLP architecture consists of:

Input Layer
     |
     ↓
Dense Layer (64 neurons)
Activation: ReLU
     |
     ↓
Dense Layer (32 neurons)
Activation: ReLU
     |
     ↓
Output Layer (1 neuron)
Activation: Sigmoid

## Layer Description

# Input Layer

The input layer receives the preprocessed and scaled features from the Breast Cancer Wisconsin dataset.

Feature scaling was applied to ensure that all input features have a similar range, improving the stability and speed of neural network training.

# Hidden Layers

The model contains two fully connected (Dense) hidden layers:

- First hidden layer: 64 neurons
- Second hidden layer: 32 neurons

Each neuron learns different patterns and relationships from the input features. The reduction in neurons from 64 to 32 helps the network gradually learn more important feature representations.

# Output Layer

The output layer contains one neuron with a sigmoid activation function.

The sigmoid function produces a probability value between 0 and 1:

- Value closer to 0 → Malignant class
- Value closer to 1 → Benign class

This makes it suitable for binary classification problems.

# 3. Activation Functions

Activation functions determine whether a neuron should be activated and introduce non-linearity into the network.

# ReLU (Rectified Linear Unit)

The hidden layers use the ReLU activation function.

Formula:

f(x) = max(0, x)

Advantages:

- Simple and computationally efficient
- Helps reduce the vanishing gradient problem
- Allows the network to learn complex patterns

ReLU outputs zero for negative values and keeps positive values unchanged, allowing faster training.

# Sigmoid Activation Function

The output layer uses the sigmoid activation function.

Formula:

σ(x) = 1 / (1 + e⁻ˣ)

Advantages:

- Produces probability values between 0 and 1
- Suitable for binary classification tasks

The sigmoid output is converted into a class prediction using a threshold value of 0.5.


# 4. Backpropagation

Backpropagation is the learning mechanism used by neural networks to improve their predictions.

The process consists of the following steps:

# 1. Forward Propagation

During forward propagation, input data passes through the network layers to generate predictions.

The model calculates an output based on current weights and biases.

# 2. Loss Calculation

The predicted output is compared with the actual output using the loss function.

For this binary classification problem, Binary Crossentropy Loss is used.

The loss value represents how far the predictions are from the actual labels.

# 3. Gradient Calculation

Backpropagation calculates the gradients of the loss function with respect to model weights using the chain rule.

These gradients indicate the direction in which weights should be adjusted to reduce errors.

# 4. Weight Update

The optimizer uses calculated gradients to update the weights and biases.

This process repeats for multiple iterations until the model learns effective patterns from the data.

# 5. Optimization Algorithm

Adam Optimizer (Adaptive Moment Estimation)

The model uses the Adam optimization algorithm for updating weights.

Adam combines the advantages of:

- Momentum optimization
- Adaptive learning rate methods

It maintains two values:

1. First moment estimate (mean of gradients)
2. Second moment estimate (variance of gradients)

These estimates help Adam adjust the learning rate for each parameter individually.

Advantages of Adam:

- Faster convergence
- Efficient for large datasets
- Requires less manual tuning
- Performs well for deep learning models

# 6. Hyperparameters Used

Parameter| Value
Model Type| Multi-Layer Perceptron
Hidden Layers| 2
First Hidden Layer| 64 neurons
Second Hidden Layer| 32 neurons
Hidden Activation| ReLU
Output Activation| Sigmoid
Optimizer| Adam
Loss Function| Binary Crossentropy
Epochs| 50
Batch Size| 32

# 7. Training Process Summary

The model was trained using scaled training data. During each epoch:

1. Training batches were passed through the network.
2. Predictions were generated through forward propagation.
3. Loss was calculated.
4. Backpropagation calculated gradients.
5. Adam optimizer updated model weights.

The model performance was evaluated using:

- Training accuracy
- Testing accuracy
- Loss value
- Precision
- Recall
- F1-score
- Confusion matrix

# 8. Conclusion

The MLP architecture successfully applies deep learning techniques for breast cancer classification. The combination of ReLU activation, sigmoid output, backpropagation, and Adam optimization 
enables the model to learn complex relationships within the dataset and achieve effective classification performance.
