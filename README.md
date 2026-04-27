# DL_cGAN_FashionMNIST

# Conditional GAN for Fashion-MNIST Image Generation

## Project Overview

This project implements a Deep Convolutional Conditional GAN (cGAN) for class-controlled image generation on the Fashion-MNIST dataset.

The generator produces clothing images conditioned on class labels, while the discriminator evaluates authenticity using spectral normalization.

## Dataset

Fashion-MNIST
60,000 training images
10 classes
28×28 grayscale

## Architecture

Generator:
Noise vector (100-dim) + class embedding
ConvTranspose layers
BatchNorm
ReLU
Tanh output

Discriminator:
Image + class embedding
Strided convolutions
Spectral normalization
LeakyReLU

## Training Details

Optimizer: Adam
Learning rate: 2e-4
Betas: (0.5, 0.999)
Epochs: 100
Loss: BCEWithLogitsLoss
Label smoothing applied

## Evaluation

FID Score: 12.28

## Experiments

Latent interpolation
Class morphing
Training stability analysis

## Results

Example outputs stored in /outputs folder

## How to Run

Open notebook:

cgan_fashion_mnist.ipynb

Run all cells sequentially
