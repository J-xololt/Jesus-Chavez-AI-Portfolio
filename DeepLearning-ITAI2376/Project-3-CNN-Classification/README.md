# Project 3: Convolutional Neural Network (CNN) for MNIST Digit Classification

## Problem Statement
Build a foundational deep learning model capable of classifying handwritten digits from the MNIST dataset. This exercise provides a hands-on understanding of CNN architecture, feature extraction, and model optimization.

## Architecture and Key Concepts

This project involves defining and training a multi-layer **Convolutional Neural Network (CNN)**.

### 1. Feature Extraction (Convolutional Layers)
* **Mechanism:** Convolutional layers use filters (kernels) to slide over input images, automatically detecting **low-level features** like edges, curves, and textures.
* **Benefit:** This structure allows the network to maintain the spatial relationships of the image data, distinguishing CNNs from traditional dense networks.

### 2. Dimensionality Reduction (Max Pooling)
* **Concept:** **Max Pooling** is applied after convolutional layers to reduce the spatial dimensions of feature maps while preserving the most prominent features.
* **Benefit:** This makes the model computationally more efficient and increases its resistance to small distortions or transformations in the input image.

### 3. Optimization and Regularization
* **Optimizer:** We utilized the **Adam Optimizer** due to its adaptive learning rate capabilities.
* **Dropout:** The **Dropout mechanism** was implemented, which randomly deactivates neurons during training. This prevents **overfitting** by forcing the network to learn more general and robust features instead of memorizing the training data.

## Reflection and Future Work
Through this lab, I gained a practical appreciation for the **feature engineering capabilities** of CNNs. I realized that the accuracy is not the sole metric; understanding how each layer contributes to feature extraction is key.

### Future Improvements (Next Steps)
1.  **Deeper Architectures:** Implement and test deeper models like **VGGNet** or **ResNet** on more complex datasets.
2.  **Transfer Learning:** Explore the concept of **Transfer Learning** (as implemented in Project 2), where a pre-trained model is adapted for a different task, significantly reducing training time.
3.  **Visual Debugging:** Implement techniques like **plotting filters and feature maps** to gain an internal view of what the network is learning at each stage.

## Source Files
* CNN Code and Notebook: `Lab04_CNN_JesusChavez_ITAI2376.pdf`
* In-depth Reflection: `Lab04_Reflection_JesusChavez_ITAI2376.pdf`
