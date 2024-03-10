# Image Retrieval System

## Overview

The Image Retrieval System is a Python-based application that leverages state-of-the-art techniques in computer vision and machine learning to perform face recognition and retrieval. 
This system employs the VGGFace architecture for feature extraction, Principal Component Analysis (PCA) for dimensionality reduction, and Faiss with inner product distance for efficient similarity search. 
The primary goal of the system is to evaluate the impact of different configurations on precision and recall in face recognition tasks.

## Components

### 1. VGGFace

The VGGFace model is used as a feature extractor. Specifically, the VGG16 architecture is employed, which is pre-trained on large face datasets. 
The system takes advantage of the learned features from this deep neural network to represent faces in a high-dimensional space.

### 2. Principal Component Analysis (PCA)

To address the high dimensionality of VGGFace features and improve efficiency, PCA is applied for dimensionality reduction. 
The system allows for experimenting with various numbers of principal components to observe the impact on face

### 3. Faiss
Faiss is a powerful library for efficient similarity search and clustering. In this system, Faiss is utilized to index and retrieve faces based on their reduced feature representations. 
