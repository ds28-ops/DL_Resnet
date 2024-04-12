# Mini-Project: Residual Nets

## Challenges
Building a ResNet architecture model from scratch to classify the CIFAR-10 dataset, with the model having no more than 5 million parameters.

## Introduction
ResNets (or Residual Networks) are one of the most commonly used models for image classification tasks. In this project, you will design and train your own ResNet model for CIFAR-10 image classification. Your goal will be to maximize accuracy on the CIFAR-10 benchmark while keeping the size of your ResNet model under budget. Model size, typically measured as the number of trainable parameters, is important when models need to be stored on devices with limited storage capacity, such as mobile devices.

## Prerequisites

## Training

## Results

| Model       | Accuracy  |
|-------------|----------:|
| Our ResNet  | 97.12%    |
| ResNet18    | 88.56%    |

## Hyperparameters in Our Final Model's Architecture

| Parameter                     | Our Model         |
|-------------------------------|-------------------|
| Number of residual layers     | 4                 |
| Number of residual blocks     | [3, 3, 3, 3]      |
| Convolutional kernel sizes    | [3, 3, 3, 3]      |
| Shortcut kernel sizes         | [1, 1, 1, 1]      |
| Number of channels            | 128, 100, 164, 200|
| Average pool kernel size      | 4                 |
| Batch normalization           | True              |
| Data augmentation             | True              |
| Data normalization            | True              |
| Lookahead                     | False             |
| Optimizer                     | SGD               |
| Learning rate (lr)            | 0.1               |
| Lr scheduler                  | CosineAnnealingLR |
| Weight decay                  | 0.0005            |
| Batch size                    | 128               |
| Number of workers             | 10                |
| Total number of Parameters    | 4,978,810         |

