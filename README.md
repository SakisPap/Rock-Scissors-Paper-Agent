# Final Project 2023 | Rock-Scissors-Paper Agent

## Overview
This project is centered around creating a Rock-Scissors-Paper agent using Machine Learning Algorithms. It was implemened as part of the educational process of [MSc. program Data and Web Science](https://dws.csd.auth.gr)

## Objectives
* Create an agent that is capable of playing the game Rock-Scissors-Paper
* Agent should be able to recognise the oponent's action and react accordingly
* The above should be applied within a context of a betting game with the Agent demonstrating high win rates (making profit)

## Key Features
* Very high percission against the test set (99%)
* Input optimization (dimensionality reduction, normalization)
* Small prediction impact against tampered (action) images
* Demonstratable prcision against action images from the Web

## Requirements
* A notebook (Google Colab, Jupyter) or a configured Python environment
* The rock-scissors-paper dataset ([Kaggle ref](https://www.kaggle.com/datasets/drgfreeman/rockpaperscissors))

## Setup and Running Instructions
You can run this directly as intended from [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1XRfqPu7L5boQafKtONTGepINVJQ8dsTO?usp=sharing)

## Architecture
After researching and experimenting with diffrenet Supervised and Deep Reinforcemen Learning techniques, the superiority of Convolutional Neural Networks (CNNs) in handling image-related tasks, backed by significant successes in the field, ultimately cemented the decision to adopt a CNN model for this task.
Here is a breakdown of the model's layers and charachteristics.
Model: "sequential_7"

| Layer (type)           | Output Shape        | Param # |
|------------------------|---------------------|---------|
| conv2d_21 (Conv2D)     | (None, 148, 148, 32)| 320     |
| max_pooling2d_14 (MaxPooling2D)| (None, 74, 74, 32)  | 0       |
| conv2d_22 (Conv2D)     | (None, 72, 72, 64)  | 18496   |
| max_pooling2d_15 (MaxPooling2D)| (None, 36, 36, 64)  | 0       |
| conv2d_23 (Conv2D)     | (None, 34, 34, 64)  | 36928   |
| flatten_7 (Flatten)    | (None, 73984)       | 0       |
| dense_14 (Dense)       | (None, 64)          | 4735040 |
| dense_15 (Dense)       | (None, 3)           | 195     |

*Total params:* 4790979 (18.28 MB)
*Trainable params:* 4790979 (18.28 MB)
*Non-trainable params:* 0 (0.00 Byte)

## Conclusion
Here is the result of an example Betting game after 100 rounds of +1$ on win and -1$ on loss. It is pretty clear that for the most part,  our agent is consistent in accurately reacting to the oponent actions and getting rich!

![](https://github.com/SakisPap/Rock-Scissors-Paper-Agent/blob/main/img/profit_proof.png)
