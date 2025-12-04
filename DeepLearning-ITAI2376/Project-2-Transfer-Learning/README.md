# Project 2: Transfer Learning for Image Classification using VGG16

## Problem Statement
The objective was to efficiently perform accurate image classification without training a massive convolutional neural network (CNN) from scratch. This was achieved by leveraging the pre-existing visual knowledge embedded in a powerful, pre-trained model.

## Approach and Methodology

### 1. Transfer Learning with VGG16
We utilized the **VGG16 architecture**, which was pre-trained on the vast **ImageNet dataset**. This model contains a high-quality encoding of general visual features. 

* **Strategy:** The pre-trained convolutional layers were kept **frozen** (non-trainable) to retain the learned features. Custom dense layers were added on top to adapt the model to the new classification task. This technique allows for rapid development and requires significantly less data.

### 2. Execution Environment & Data Preprocessing
The code was executed within a **Google Colab Notebook** (as indicated in the source file). Successful utilization of VGG16 requires strict input adherence:
* **Resizing:** All input images were resized to the required **$224 \times 224$ pixels**.
* **Normalization:** Pixel values were processed using `preprocess_input` to match the scaling used during the original ImageNet training.

## Results and Evaluation
* The model successfully demonstrated high accuracy in classifying complex, real-world images.
* **Key Finding:** Experiments showed that the model's predictions are highly sensitive to input transformations (such as rotation or noise), highlighting its dependence on the specific visual patterns learned during its initial ImageNet training.

## Learning Outcomes
* Mastered the practical application of **Transfer Learning** using pre-trained weights to solve new computer vision problems.
* Gained proficiency in the essential **data preprocessing and normalization** steps required when working with large, pre-trained models.

## Source Code
* Colab Notebook Printout: `L02_Jesus_Chavez_ITAI2376.pdf`
