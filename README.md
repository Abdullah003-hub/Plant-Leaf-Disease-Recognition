A Modular Vision Pipeline for Multiclass Plant Leaf Disease Recognition
Project Overview
The project is structured as a modular pipeline that demonstrates the evolution of computer vision techniques. 
It begins with low-level image restoration, moves into classical feature engineering, and culminates in a deep learning 
classification model with interpretability features.

Module 1: Foundations of Vision
This module focuses on the essential preprocessing steps required to enhance image quality. It includes:

Transformations: Implementation of geometric scaling, rotations, and intensity adjustments like Gamma Correction and Histogram Equalization.

Noise & Restoration: Techniques for adding and removing Gaussian and Salt & Pepper noise using Bilateral and Median filtering.

Edge Detection: Comparative analysis of structural features using the Canny edge detector.

Module 2: Classical Feature-Based Vision
This section explores "hand-crafted" features and unsupervised learning:

Descriptor Extraction: Computing HOG (Histogram of Oriented Gradients), LBP (Local Binary Patterns), and GLCM (Gray-Level Co-occurrence Matrix) to represent leaf textures.

Clustering: Utilizing PCA (Principal Component Analysis) for dimensionality reduction followed by K-Means clustering to group similar leaf patterns.

Keypoint Detection: Identifying unique leaf landmarks using SIFT and FAST detectors.

Module 3: Deep Learning & Interpretability
The final module implements a robust classification system using Transfer Learning:

Architecture: A MobileNetV2 backbone is utilized for efficient feature extraction, followed by a custom-trained dense classifier head.

Optimization: The model employs a two-phase training strategy, including initial training of the head and subsequent fine-tuning of the base layers.

Explainability: Integration of Saliency Maps to visualize the specific regions of the leaf that influence the model's diagnostic decision.

Technical Stack
To ensure the pipeline operates efficiently across preprocessing, feature extraction, and neural network training, the following libraries are required:

OpenCV-Python: Used as the primary engine for image manipulation, colorspace conversions (RGB to HSV), and implementing classical vision algorithms like Canny and SIFT.

NumPy: Facilitates high-performance numerical operations and matrix manipulations essential for handling image data as arrays.

Matplotlib: Employed for the comprehensive visualization of results, including side-by-side comparisons of filtered images, clusters, and training curves.

Scikit-Image: Provides advanced image processing routines such as Local Binary Pattern (LBP) extraction and structural similarity indexing.

Scikit-Learn: Powering the machine learning components, specifically for PCA dimensionality reduction and the K-Means clustering algorithm.

TensorFlow: The core framework used to build, train, and deploy the deep learning models, including the implementation of the MobileNetV2 architecture and gradient-based saliency maps.

Installation & Usage::
Clone this repository:
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
Install the required dependencies:
pip install opencv-python numpy matplotlib scikit-image scikit-learn tensorflow
Run the main pipeline

----------------------------------------------------------------------------
