# Image Retrieval System

## Overview

The Image Retrieval System is a Python-based application that leverages state-of-the-art techniques in computer vision and machine learning to perform face recognition and retrieval. 
This system employs the VGGFace architecture for feature extraction, Principal Component Analysis (PCA) for dimensionality reduction, and Faiss with inner product distance for efficient similarity search. 
The primary goal of the system is to evaluate the impact of different configurations on precision and accuracy in face recognition and retrieval tasks.

## Components

### 1. VGGFace

The VGGFace model is used as a feature extractor. Specifically, the VGG16 architecture is employed, which is pre-trained on large face datasets. 
The system takes advantage of the learned features from this deep neural network to represent faces in a high-dimensional space.

### 2. Principal Component Analysis (PCA)

To address the high dimensionality of VGGFace features and improve efficiency, PCA is applied for dimensionality reduction. 
The system allows for experimenting with various numbers of principal components to observe the impact.

### 3. Faiss
Faiss is a powerful library for efficient similarity search and clustering. In this system, Faiss is utilized to index and retrieve faces based on their reduced feature representations. 

## Usage
1. **Balancing Dataset**: To balance the dataset, you can use the init_balanced_dataset() function. This function takes the LFW dataset (lfw_people) and balances it based on the minimum number of elements per class. It returns the balanced data and targets.

2. **Image Normalization** and Standardization: Before feature extraction, it's essential to normalize and standardize the images. The compute_features() function accomplishes this task. It also extracts features using VGGFace model if specified.

3. **Create Reduction**: The create_test_reduction() function creates PCA reduction for feature vectors. It returns PCA object, reduced features, and Faiss index.

4. **Create Tests**: Use the create_test() function to create tests with varying numbers of PCA components. It returns PCA objects, feature vectors, and Faiss indices.

5. **Compute Precision-Recall**: The compute_precision_recall() function calculates precision and recall for retrieval tasks.

6. **Predict**: Use the predict() function to predict labels for test data.

7. **Compute Precision-Recall (All)**: The compute_all_precision_recall() function computes precision and recall for all retrieval tasks.

8. **Create DataFrame**: This utility function creates a DataFrame from computed precision and recall values.

9. **Create List DataFrame**: Creates a list of DataFrames for various retrieval tasks.

10. **Merge DataFrame**: Merges DataFrames into a single DataFrame for easy comparison.
