# Attack_Defense_CNN

This repository contains the code for implementing adversarial training as a defense mechanism against adversarial attacks in deep neural networks. The defense is based on the Fast Gradient Sign Method (FGSM) using the Foolbox library.

## Tools Used

- **PyTorch:** Deep learning library used for building and training neural networks.
- **Foolbox:** Python library for creating adversarial examples and evaluating robustness of machine learning models.

## How it Works

The adversarial training process involves creating adversarial examples during the training phase to improve the model's robustness against potential attacks. The following steps outline the workflow:

1. **Model Initialization:**
   - Initialize the defense model using PyTorch.
   - Load the training data using a PyTorch DataLoader.

2. **Adversarial Example Generation:**
   - Convert the PyTorch model to a Foolbox model.
   - Use Foolbox's FGSM attack to generate adversarial examples for each input image.

3. **Training with Adversarial Examples:**
   - Incorporate adversarial examples into the training set.
   - Train the defense model on the combined dataset.

4. **Evaluation:**
   - Evaluate the trained model on both clean and adversarial test datasets.
