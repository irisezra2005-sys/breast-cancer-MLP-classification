# breast-cancer-MLP-classification

# Breast Cancer Classification using Neural Network (MLP)

## Project Overview

This project implements a **Multi-Layer Perceptron (MLP) Neural Network** to classify breast cancer cases as **malignant** or **benign** using the Breast Cancer Wisconsin dataset.

The objective of this project is to build, train, and evaluate a deep learning classification model while understanding the impact of neural network architecture, hyperparameters, and feature scaling on model performance.


# Dataset Description

**Dataset:** Breast Cancer Wisconsin Diagnostic Dataset

The dataset contains numerical features computed from digitized images of breast mass samples.

### Features:
- Mean radius
- Mean texture
- Mean perimeter
- Mean area
- Mean smoothness
- Mean compactness
- Mean concavity
- And other cell nucleus characteristics

### Target:
- **0 → Malignant**
- **1 → Benign**

# Data Preprocessing

The following preprocessing steps were applied:

- Dataset loading
- Checking missing values
- Splitting data into training and testing sets
- Feature scaling using **StandardScaler**
- Preparing data for neural network input

### Data Split:

- Training data: 80%
- Testing data: 20%


# Neural Network Architecture

The classification model is built using a **Multi-Layer Perceptron (MLP)**.

### Architecture:

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

### Explanation:

- **Input Layer:** Receives scaled dataset features.
- **Hidden Layers:** Learn complex patterns from input features.
- **ReLU Activation:** Introduces non-linearity and improves learning.
- **Output Layer:** Uses sigmoid activation for binary classification.

# Hyperparameters

| Parameter | Value |
|-----------|-------|
| Model Type | Multi-Layer Perceptron (MLP) |
| Optimizer | Adam |
| Loss Function | Binary Crossentropy |
| Activation Function | ReLU |
| Output Activation | Sigmoid |
| Number of Hidden Layers | 2 |
| Neurons in First Hidden Layer | 64 |
| Neurons in Second Hidden Layer | 32 |
| Batch Size | 32 |
| Epochs | 50 |
| Validation Split | 20% |


# Model Training

The model was trained using the scaled training dataset.

During training, the model performance was monitored using:

- Training accuracy
- Validation accuracy
- Training loss
- Validation loss

Training curves were generated to analyze model learning behaviour.

# Training Results

## Model Performance

| Metric | Score |
|--------|-------|
| Training Accuracy |100%|
| Testing Accuracy | 96% |
| Loss |3%|


# Visualizations

### Accuracy Curve

Shows the improvement of training and validation accuracy over epochs.


### Loss Curve

Shows reduction in training and validation loss during training.

### Confusion Matrix

Displays the classification performance between malignant and benign cases.


# Evaluation Metrics

The model was evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

These metrics provide a detailed understanding of classification performance.

# Results & Findings

- The MLP model successfully learned patterns from the breast cancer dataset.
- Feature scaling improved neural network training stability.
- The model achieved strong classification performance on unseen test data.
- The confusion matrix shows effective separation between malignant and benign cases.



# Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn


# Future Improvements

- Hyperparameter tuning
- Adding dropout layers to reduce overfitting
- Testing different neural network architectures
- Using cross-validation for better evaluation
