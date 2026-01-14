
# AlexNet Implementation for CIFAR-10

## Overview
This project implements the AlexNet Convolutional Neural Network architecture adapted for the CIFAR-10 dataset. Here's the accompanying [blog](https://tonar.xyz/blog/2025/alexnet-implementation/) to the project.AlexNet was a groundbreaking CNN architecture that won the ImageNet Large Scale Visual Recognition Challenge (ILSVRC) in 2012, significantly outperforming previous approaches and helping to usher in the deep learning revolution in computer vision.

## Features
- Complete implementation of AlexNet architecture adapted for smaller 32x32 CIFAR-10 images
- Advanced data augmentation techniques including:
    - Random cropping with padding
    - Horizontal flipping
    - PCA-based color augmentation (as described in the original AlexNet paper)
    - Standard color jittering
- Local Response Normalization (LRN) as used in the original paper
- Dropout regularization to prevent overfitting
- Learning rate scheduling
- Gradient clipping for stable training

## Dataset
The implementation uses the CIFAR-10 dataset, which consists of 60,000 32x32 color images across 10 classes:

- Airplane
- Automobile
- Bird
- Cat
- Deer
- Dog
- Frog
- Horse
- Ship
- Truck

The dataset is automatically downloaded and split into training and testing sets.


## Model Architecture
The AlexNet architecture has been adapted to work with the smaller 32x32 CIFAR-10 images (compared to the original 224x224 ImageNet images).

## Data Augmentation
The implementation includes several data augmentation techniques to improve model generalization:

1. Random Cropping : Images are padded by 4 pixels and then randomly cropped back to 32x32
2. Random Horizontal Flipping : Images are randomly flipped horizontally with 100% probability
3. PCA-based Color Augmentation : Color perturbation along principal component axes of RGB values, as described in the original AlexNet paper
4. Normalization : Images are normalized using the dataset mean and standard deviation


## Training Details
- Optimizer : Stochastic Gradient Descent (SGD) with momentum
- Learning Rate : Starting at 0.01 with step decay
- Weight Decay : 5e-4 for regularization
- Loss Function : Cross-Entropy Loss
- Gradient Clipping : Applied to prevent exploding gradients


## Requirements
## Usage
The entire implementation is contained in the Jupyter notebook AlexNet_Implementation.ipynb . To run it:

1. Ensure you have all the required dependencies installed
2. Open the notebook in Jupyter or Google Colab
3. Run all cells sequentially

## References
1. Krizhevsky, A., Sutskever, I., & Hinton, G. E. (2012). ImageNet classification with deep convolutional neural networks. In Advances in neural information processing systems (pp. 1097-1105).
2. CIFAR-10 dataset: https://www.cs.toronto.edu/~kriz/cifar.html
3. My blog on the implementation of this paper: https://tonar.xyz/blog/2025/alexnet-implementation/
