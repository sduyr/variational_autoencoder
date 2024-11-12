# Variational Autoencoder (VAE) for Image Generation

This project demonstrates a **Variational Autoencoder (VAE)**, a generative neural network that learns a compressed, probabilistic representation of images. Once trained, a VAE can be used to generate new images and explore smooth transitions 
between images using interpolation in the latent space.

---

## Project Overview

This VAE project focuses on:
- **Encoding Images** into a compressed latent space.
- **Generating New Images** by sampling from this latent space.
- **Latent Space Interpolation** to transition smoothly between images.

---

## Key Concepts

### 1. Variational Autoencoder (VAE)
A VAE consists of three main components:
- **Encoder**: Compresses input images into a mean (`μ`) and a log variance (`log σ²`).
- **Reparameterization Trick**: Allows sampling from the latent space while maintaining differentiability for backpropagation.
- **Decoder**: Reconstructs images from the latent space back to the input space.

### 2. Loss Function
The VAE uses a combination of two losses:
- **Reconstruction Loss**: Measures how well the reconstructed image matches the input.
- **KL Divergence**: Regularizes the latent space to approximate a standard normal distribution (`N(0,1)`).

### 3. Latent Space Interpolation
By moving through the latent space between two or more points, we can create smooth transformations between images, helping us understand how different features are encoded.

---

## Setup and Requirements

To run this project, you will need:
- **Python 3.7+**
- **PyTorch**
- **Torchvision**
- **Matplotlib** for visualizing images

Install the requirements:
```bash
pip install torch torchvision matplotlib
