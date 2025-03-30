# MNIST Image Classification Using CNN, KNN, SVM, and Naive Bayes


<img src="header.png" alt="TOC" style="width: auto; max-width: 100%;">


## Project Overview

This project demonstrates the implementation and comparison of several machine learning algorithms on the **MNIST dataset**, including Convolutional Neural Networks (CNN), K-Nearest Neighbors (KNN), Support Vector Machines (SVM), and Multinomial Naive Bayes (NB). The objective is to evaluate and compare their performance on the task of handwritten digit classification.

## Technologies Used

* **TensorFlow (Keras)**: For building and training the CNN model.
* **Scikit-learn**: For implementing KNN, SVM, and Naive Bayes models.
* **NumPy**: For numerical operations and array handling.
* **Pandas**: For data manipulation.
* **Matplotlib/Seaborn**: For data visualization.
* **Joblib**: For saving trained models to disk.

## Dataset

The MNIST dataset consists of 60,000 training images and 10,000 testing images of handwritten digits. Each image is 28x28 pixels in grayscale.

* **Training set**: 60,000 images
* **Test set**: 10,000 images
* **Image size**: 28x28 pixels
* **Number of classes**: 10 (digits 0 to 9)

## Models Implemented

### CNN (Convolutional Neural Networks)

**Architecture**:
* Two convolutional layers with ReLU activation and MaxPooling for feature extraction.
* A Flattening layer followed by a fully connected (dense) layer.
* Dropout regularization is applied to prevent overfitting.
* The final layer uses a Softmax activation function for classifying the digits.

Data augmentation techniques like rotation, zoom, and shifts were applied to improve model generalization.

### KNN (K-Nearest Neighbors)

The KNN model uses a flattened version of the 28x28 images, converting them into a 1D vector (784 features). The class is assigned based on majority voting among the K nearest neighbors.

### SVM (Support Vector Machines)

The SVM classifier is trained on flattened images with a radial basis function (RBF) kernel to find the optimal hyperplane that separates different digit classes with a maximum margin.

### Naive Bayes

A Multinomial Naive Bayes classifier is used, assuming conditional independence between pixel values. It’s simple but fast for classification.

## Performance Comparison

| Model          | Accuracy   |
|----------------|------------|
| **CNN**        | 99.41%     |
| **KNN**        | 97.17%     |
| **SVM**        | 94.04%     |
| **Naive Bayes**| 83.57%     |

**Key Observations**:
* **CNN** outperformed the other models with an accuracy of **99.41%**, demonstrating the effectiveness of deep learning techniques for image classification.
* **KNN** performed well but is computationally expensive for large datasets.
* **SVM** had good accuracy, but fell short compared to CNN and KNN.
* **Naive Bayes** had the lowest accuracy due to the assumption of independent features.

## Installation

To run this project locally, you need to install the required dependencies. Ensure you have Python installed, then run the following command:

pip install -r requirements.txt


## Usage

1. **Download the Dataset**: Ensure the MNIST dataset is available, either from TensorFlow datasets or manually.
2. **Run the Jupyter Notebook**: The entire project is contained in a single Jupyter notebook.


This will open the notebook in your browser. You can execute all the cells to preprocess data, train models, and evaluate their performance.

## Results

The results of the model comparison are as follows:

* **CNN**: Highest accuracy (99.41%) with robust generalization capabilities.
* **KNN**: Strong performance (97.17%) but computationally expensive.
* **SVM**: Achieved an accuracy of 94.04%.
* **Naive Bayes**: Fast but underperformed due to its simplicity.

## Visualizations

You can view visualizations of the model performances directly within the Jupyter notebook, including accuracy plots and confusion matrices.


