🚀 Smooth Activation Functions Analysis using ResNet-18 on CIFAR-10

📌 Overview

This project explores the impact of smooth activation functions on deep learning performance using a ResNet-18 architecture trained on the CIFAR-10 dataset.

We compare traditional and modern activation functions to analyze their effect on:

Model accuracy 📈
Convergence speed ⚡
Classification performance 

🎯 Objective

To evaluate whether smooth activation functions (GELU, Swish, Mish) outperform the traditional ReLU in image classification tasks.

🧠 Activation Functions Compared
🔹 ReLU (Baseline)
Simple and fast
Most widely used
Can suffer from dying ReLU problem

🔹 GELU (Gaussian Error Linear Unit)
Used in modern architectures like Transformers
Smooth and probabilistic behavior

🔹 Swish
Proposed by Google
Smooth and non-monotonic

🔹 Mish
Self-regularized activation
Smooth and maintains small negative values

📂 Dataset: CIFAR-10

60,000 images (32x32 RGB)
10 classes:
Airplane ✈️
Automobile 🚗
Bird 🐦
Cat 🐱
Deer 🦌
Dog 🐶
Frog 🐸
Horse 🐴
Ship 🚢
Truck 🚚

⚙️ Tech Stack

Python 🐍

PyTorch 🔥

TorchVision

NumPy

Matplotlib

Seaborn

Scikit-learn

💻 Device Configuration

device = torch.device("cuda" if torch.cuda.is_available() else "cpu")
Automatically uses GPU if available
Falls back to CPU otherwise

🏗️ Model Architecture

Base Model: ResNet-18

Modifications:

Adjusted for CIFAR-10 (32x32 images)

Removed max pooling layer

Custom activation replacement

Final layer adapted for 10 classes

🔄 Workflow
Load CIFAR-10 dataset

Apply normalization & transformations

Define custom activation functions

Replace ReLU in ResNet with selected activation

Train model for each activation

Evaluate using:

Accuracy

Confusion Matrix

Compare performance across activations

📊 Results & Visualization

📈 Accuracy Comparison

Plots test accuracy across epochs for each activation

📉 Confusion Matrix

Shows classification performance per class

🏆 Best Activation Selection

Automatically identifies the best-performing activation function

📈 Output

Training & testing accuracy per epoch
Accuracy comparison graph
Confusion matrices for each activation
Best activation function printed

🏆 Expected Insights

Smooth activation functions often:
Improve gradient flow
Provide better convergence
Achieve slightly higher accuracy
