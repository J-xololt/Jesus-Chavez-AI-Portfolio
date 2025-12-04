# 🖼️ Project: Denoising Diffusion Probabilistic Model (DDPM) for Image Generation

## Problem Statement
The goal of this assignment was to implement a **Generative AI** model capable of synthesizing novel, realistic handwritten digits (from the MNIST dataset) from pure random noise. This project demonstrates mastery of current, complex generative modeling techniques.

## Approach and Methodology

### 1. Model Architecture
The core system is the **U-Net architecture** 

. This is crucial for diffusion because its **encoder-decoder structure with skip connections** allows the model to:
* **Encoder/Decoder:** Compress input for high-level feature extraction and then gradually restore the image (denoising).
* **Skip Connections:** Preserve fine-grained image details, preventing the loss of crucial features (like digit borders) during the noise prediction process.

### 2. The Diffusion Process
* **Forward Diffusion:** Gaussian noise is sequentially added to the images over 100 time steps.
* **Reverse Process (Training):** The U-Net is trained to predict the noise that was added at each specific time step. The **Time Embedding** technique is used to inform the U-Net of the current noise level.
* **Loss Function:** The model is optimized using the **Mean Squared Error (MSE)** loss.

### 3. Advanced Techniques & Conditioning
* **Class Conditioning:** **Classifier-free guidance** was implemented by converting the desired digit (0-9) into a spatial feature map using a one-hot vector. This allows the model to be guided to generate a specific, targeted digit.
* **Evaluation:** Model quality was evaluated using **CLIP scores**, which measure the semantic agreement between the generated image and its text prompt.

## Results and Evaluation
* **Performance:** Achieved low **Mean Squared Error (MSE)** loss, indicating high effectiveness in noise prediction and removal.
* **Qualitative Findings:** Generated samples show a clear progression from noise to recognizable digits.
* **CLIP Score Analysis:** Simpler numbers consistently achieved higher CLIP scores than complex digits, confirming what the evaluation model considered "high quality."

## Learning Outcomes
* Mastered the theory and implementation of **Denoising Diffusion Probabilistic Models (DDPMs)**.
* Gained practical expertise in implementing the **U-Net architecture** and its crucial role in image synthesis.
* Developed skills in advanced Generative AI evaluation using contemporary metrics like **CLIP scores** and techniques like **Classifier-Free Guidance**.

## Requirements and Dependencies
To run the included code, you need the following:
```text
tensorflow>=2.x
keras
numpy
matplotlib
