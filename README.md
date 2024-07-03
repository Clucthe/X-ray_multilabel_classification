# Medical Image Classification using DenseNet121
This project classifies medical images into various categories using a convolutional neural network (DenseNet121). The dataset consists of medical images categorized into 15 different classes. This README provides instructions on setting up the project, understanding the code, and running the model.

## Table of Contents
  1. Requirements
  2. Dataset - https://drive.google.com/drive/folders/1XkVgaz-6n82JjRdrZv3eOLXD3Toc9TMt?usp=drive_link
  3. Code Explanation
  4. Results
  5. References

## Requirements
Before running the code, ensure you have the following packages installed:

keras, 
tensorflow, 
opencv-python, 
numpy, 
pandas, 
matplotlib, 
scikit-learn

You can install these packages using pip:

    pip install keras tensorflow opencv-python numpy pandas matplotlib scikit-learn
    
## Dataset
The dataset should be organized in the following structure:

    Dataset/
    ├── Cardiomegaly/
    │   ├── image1.png
    │   ├── image2.png
    │   └── ...
    ├── Emphysema/
    │   ├── image1.png
    │   ├── image2.png
    │   └── ...
    ├── ...
    └── Consolidation/
        ├── image1.png
        ├── image2.png
        └── ...
Ensure that the dataset directory is correctly set in the code (dataset_path = 'Dataset').

## Code Explanation
  ### 1. Data Loading and Preprocessing:

The images are loaded from the dataset directory.
Each image is resized to 32x32 pixels.
The images are normalized, and labels are one-hot encoded.

  ### 2.Data Augmentation:

Data augmentation is selectively applied to classes with fewer images to balance the dataset.

  ### 3.Model Definition:

A DenseNet121 model pre-trained on ImageNet is used.
Custom layers are added on top of the base model for the classification task.

  ### 4.Model Compilation:

The model is compiled using the Adam optimizer and binary cross-entropy loss.

  ### 5.Model Training:

The model is trained on the training dataset and validated on the validation dataset.
  ### 6.Evaluation:

The model is evaluated on the test dataset.
Confusion matrix and classification report are generated.

## Results
  1. The model's performance on the test set will be displayed, including test loss and accuracy.
  2. Classification report and confusion matrix will provide insights into the model's performance on each class.

## References
  1. DenseNet121 - https://keras.io/api/applications/densenet/
  2. Keras Documentation - https://keras.io/
  3. TensorFlow Documentation - https://www.tensorflow.org/
  4. OpenCV Documentation - https://docs.opencv.org/
  5. Scikit-learn Documentation - https://scikit-learn.org/
