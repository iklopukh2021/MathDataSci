# Problem Set 3

In this project, we explored the process of flower classification using the AlexNet deep learning model. We loaded the Flower 102 dataset, fine-tuned the pre-trained AlexNet model, and performed inference on a set of images. This report outlines the steps we followed and the results we obtained.

## Code

Notebook: https://colab.research.google.com/drive/1yhRf24-CkmZs7L3TF5wQ-eomHkmmf4ft?usp=sharing

## Dataset and Data Preparation

We started by downloading the Flower 102 dataset, which consists of 102 different categories of flowers. The dataset was divided into training and validation sets. To prepare the data for training and validation, we performed the following steps:

1. Downloaded and extracted the Flower 102 dataset, which contains images of various flower species.

2. Defined data transformations, including resizing, cropping, and normalizing the images, to be used during both training and validation.

3. Created PyTorch `DataLoader` objects for both the training and validation sets.

4. Checked the dimensions of the loaded images and labels to ensure data correctness.

## Inference with Pre-trained AlexNet

We employed a pre-trained AlexNet model for inference on a set of flower images from the dataset. For each image, we followed these steps:

1. Loaded the image onto the same device (GPU or CPU) as the AlexNet model.

2. Passed the image through the model to obtain class scores for each of the 102 categories.

3. Extracted the class with the highest score as the predicted class and printed it.

4. Displayed the image along with its true label for visual inspection.

## Model Fine-Tuning

To adapt the pre-trained AlexNet model for flower classification, we made the following adjustments:

1. Modified the last fully connected layer to have 102 output features, corresponding to the 102 flower categories in the dataset.

2. Defined the loss function as the cross-entropy loss and the optimizer as Stochastic Gradient Descent (SGD).

3. Specified a learning rate and momentum for the optimizer.

4. Trained the model for multiple epochs on the training dataset, periodically evaluating its performance on the validation set.

5. Monitored and recorded the training and validation loss and accuracy for each epoch.

## Results

Here are some of the results we obtained from our flower classification task:

- After fine-tuning the model for several epochs, we achieved an accuracy of approximately 88% on the validation dataset. This high accuracy indicates that the model was able to effectively classify flowers.

- The accuracy increased as the number of training epochs progressed, suggesting that the model continued to learn and improve its performance.

- For inference on selected images, the model provided predictions that were mostly accurate. The predicted class labels generally matched the actual flower species depicted in the images.

## Conclusion

In this project, we successfully fine-tuned a pre-trained AlexNet model for flower classification using the Flower 102 dataset. The model exhibited strong performance, with an accuracy of approximately 95%, in differentiating between various flower species. This example demonstrates the power of transfer learning when dealing with deep learning models and datasets.

The trained model can be saved and deployed for various applications, such as automating the classification of flower images in real-world scenarios.
