# Diffusion-Based Conditional Generative Model

This project implements a **Diffusion-Based Conditional Generative Model** for image synthesis, allowing the generation of images conditioned on class labels. The model is inspired by Denoising Diffusion Probabilistic Models (DDPM) and is adapted to generate class-specific outputs using label conditioning.

## 📌 Overview

Diffusion models learn to reverse a gradual noising process to generate data from random noise. In this project, we:
- Implement a forward diffusion process to add noise to images.
- Train a neural network to reverse this process conditioned on labels.
- Generate new images by sampling from noise, guided by class information.

## 🧠 Model Architecture

I use a simplified **UNet** architecture to predict the noise added at each timestep. The model is trained using Mean Squared Error (MSE) loss between the predicted and actual noise values. The conditioning is achieved by embedding class labels and injecting them into the network at multiple levels.

## 🧪 Dataset

- **MNIST**: Handwritten digits (0–9).
- Images are 28x28 grayscale.
- Each image is used with its label to condition the generation process.

## ✅ Results

The model successfully learns to generate digit images conditioned on labels and achieves an accuracy of 95%.

**Observations:**
- The quality of generated digits improves as training progresses.
- The conditional control is effective — digits generated match their specified class.
- Even with a simple UNet and limited training steps, the model produces diverse and realistic digit samples.

## 🖼️ Output
**Class = 9**

<img width="256" height="256" alt="generated_class_9_big" src="https://github.com/user-attachments/assets/74b0e30a-c139-4a27-b97f-eebb7a0cec42" />

