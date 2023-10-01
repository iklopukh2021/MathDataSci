# Problem Set 1 Report

## Introduction

In this assignment, I implemented a simple neural network using PyTorch and trained it on the MNIST dataset to classify handwritten digits. The goal was to understand the basics of building and training neural networks using PyTorch.

## Code Overview

Notebook:
https://colab.research.google.com/drive/1ladfI7rRt0A1z6DRiBx0Mu9-vbPmHIVE?usp=sharing

### Importing Libraries

I began by importing the necessary libraries, including NumPy, Matplotlib, Torch, and torchvision.

### Data Preparation

We loaded the MNIST dataset using torchvision and preprocessed the data by normalizing pixel values to the range [0, 1]. We also defined functions to work with GPU tensors for better performance.

### Data Visualization

I created functions to visualize data, including individual images and image montages, to help understand the dataset.

Here is an image of the data visualization:
![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/78235dbd-91cb-430b-8be3-abc629b1ef29)

### Training the Model

I implemented a simple neural network model that takes flattened input images and predicts the digit class. I defined a random weight matrix `M` and used it to transform the input data `x`. The transformed data `y` was then used to predict the digit class. I trained the model by adjusting the weight matrix `M` to maximize the accuracy of the predictions.

## Results

- Initial accuracy on a small subset of the dataset: 7.81%
- After training for several iterations, I achieved an accuracy of 69.06% using a random weight matrix `M`.
- I further improved the accuracy to 85.95% by adjusting the weight matrix `M` through gradient ascent on the entire dataset.

## Conclusion

In this assignment, I successfully implemented a simple neural network using PyTorch and trained it on the MNIST dataset to classify handwritten digits. I learned how to preprocess data, build a basic neural network model, and optimize it using gradient ascent. The final accuracy of 85.95% demonstrates the effectiveness of the approach.

Overall, this assignment provided valuable experience in working with PyTorch and understanding the fundamentals of neural network training.
