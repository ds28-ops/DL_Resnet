# Mini-Project: Residual Nets

## Challenges
Building a ResNet architecture model from scratch to classify the CIFAR-10 dataset, with the model having no more than 5 million parameters.

## Introduction
ResNets (or Residual Networks) are one of the most commonly used models for image classification tasks. In this project, you will design and train your own ResNet model for CIFAR-10 image classification. Your goal will be to maximize accuracy on the CIFAR-10 benchmark while keeping the size of your ResNet model under budget. Model size, typically measured as the number of trainable parameters, is important when models need to be stored on devices with limited storage capacity, such as mobile devices.

## Repo Schema
* Models folder has all our pre-trained models. The good, bad, and the ugly.
* Notebooks folder has the 3 notebooks  with the best performance. 
* Requirements.txt has all the required libraries
* README, well, you know.

## Run
To train the models, the cells in each notebook should be run in order. The notebooks are available in the Notebooks folder.


## Results

| Model         | Accuracy  |
|---------------|-----------|
| ResNet26_97   | 97.12%    |
| ResNet24_9684 | 96.84%    |
| ResNet24_96   | 96.57%    |
| ResNet18*     | 88.56%    |

* Performance of Official ResNet18 architecture.

## Hyperparameters in Our Final Model's Architecture

| Parameter                     | Best Model 1 - ResNet26_97    | Best Model 2 - ResNet24_9684 |  Best Model 3 - ResNet24_9684 |
|-------------------------------|-------------------------------|------------------------------|-------------------------------|
| Number of residual layers     | 4                             |4                             |4                              |
| Number of residual blocks     | [3, 3, 3, 3]                  |[3, 3, 2, 3]                  |[3, 3, 2, 3]                   |
| Convolutional kernel sizes    | [3, 3, 3, 3]                  |[3, 3, 3, 3]                  |[3, 3, 3, 3]                   |
| Shortcut kernel sizes         | [1, 1, 1, 1]                  |[1, 1, 1, 1]                  |[1, 1, 1, 1]                   |
| Number of channels            | 128, 100, 164, 200            |138, 100, 204, 190            |136, 100, 188, 204             |
| Average pool kernel size      | 4                             |4                             |4                              |
| Batch normalization           | True                          |True                          |True                           |
| Data augmentation             | Flip, Crop, Perspective, Auto |Flip, Crop, Perspective, Auto |Flip, Crop, Perspective, Auto  |
| Data normalization            | True                          |True                          |True                           |
| Optimizer                     | SGD + Momentum                |SGD + Momentum                |AdamW                          |
| Learning rate (lr)            | 0.1                           |0.1                           |0.1                            |
| Lr scheduler                  | CosineAnnealingLR             |CosineAnnealingLR             ||CosineAnnealingLR             |
| Weight decay                  | 0.0005                        |0.0005                        |0.0005                         |
| Batch size                    | 128                           |128                           |128                            |
| Number of workers             | 14                            |10                            |14                             |
| Total number of Parameters    | 4,978,810                     |4,969,776                       |4,997,074                        |


## Everything about all our models
This google sheet has all the architectures we tried and tested. 
https://shorturl.at/tzAC5
