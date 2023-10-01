# Problem Set 1 Report

## Introduction

In this assignment, we implemented a simple neural network using PyTorch and trained it on the MNIST dataset to classify handwritten digits. The goal was to understand the basics of building and training neural networks using PyTorch.

## Code Overview

### Importing Libraries

We began by importing the necessary libraries, including NumPy, Matplotlib, Torch, and torchvision. Additionally, we installed the WandB library for experiment tracking.

### Data Preparation

We loaded the MNIST dataset using torchvision and preprocessed the data by normalizing pixel values to the range [0, 1]. We also defined functions to work with GPU tensors for better performance.

### Data Visualization

We created functions to visualize data, including individual images and image montages, to help us understand the dataset.
![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/78235dbd-91cb-430b-8be3-abc629b1ef29)

### Training the Model

We implemented a simple neural network model that takes flattened input images and predicts the digit class. We defined a random weight matrix `M` and used it to transform the input data `x`. The transformed data `y` was then used to predict the digit class. We trained the model by adjusting the weight matrix `M` to maximize the accuracy of the predictions.

## Results

- Initial accuracy on a small subset of the dataset: 7.81%
- After training for several iterations, we achieved an accuracy of 69.06% using a random weight matrix `M`.
- We further improved the accuracy to 85.95% by adjusting the weight matrix `M` through gradient ascent on the entire dataset.

## Conclusion

In this assignment, we successfully implemented a simple neural network using PyTorch and trained it on the MNIST dataset to classify handwritten digits. We learned how to preprocess data, build a basic neural network model, and optimize it using gradient ascent. The final accuracy of 85.95% demonstrates the effectiveness of the approach.

Overall, this assignment provided valuable experience in working with PyTorch and understanding the fundamentals of neural network training.

Please note that this report provides a high-level overview of the assignment. For detailed code and results, refer to the provided Jupyter Notebook.
