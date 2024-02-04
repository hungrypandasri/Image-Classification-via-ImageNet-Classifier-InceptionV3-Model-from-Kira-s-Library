# Project: Adversarial Attacks on Self-Driving Car Neural Networks

## Overview
This project explores the robustness of neural networks, specifically focusing on self-driving car models, through visualization, adversarial attacks, and probabilistic robustness evaluation. The experiments utilize pre-trained models such as ResNet-18 and AlexNet.

## Table of Contents
1. [Introduction](#introduction)
2. [Model](#model)
    - [Neural Network Visualization](#neural-network-visualization)
    - [Adversarial Example](#adversarial-example)
    - [Probabilistic Robustness Evaluation](#probabilistic-robustness-evaluation)
3. [Resources](#resources)
    - [Dataset](#dataset)
4. [Code Structure](#problem-set)
    - [ 1: Adversarial Example Generation](#exercise-1-adversarial-example-generation-for-resnet-18)
    - [ 2: Neural Network Visualization](#exercise-2-neural-network-visualization)
    - [ 3: Evaluation of Probabilistic Robustness](#exercise-3-evaluation-of-probabilistic-robustness)
5. [Reference](#reference)

## Introduction
This project provides a hands-on opportunity to assess AI robustness by visualizing neural network layers, generating adversarial examples, and estimating the robustness of a self-driving car neural network when subjected to random perturbations.

## Model
### Neural Network Visualization
Visualization techniques include activation maximization and saliency maps for Convolution Neural Network (CNN) layers. Tools like FlashTorch and MapExtrackt are employed for this purpose.

### Adversarial Example
Simple adversarial attacks, both targeted and untargeted, are implemented on a pretrained ResNet-18 model using the ScratchAI package. The goal is to perturb the input image to induce misclassifications.

### Probabilistic Robustness Evaluation
Probabilistic robustness is measured by assessing the network's performance when inputs are subject to random perturbations. Monte Carlo (MC) sampling is used to estimate the misclassification rate.

## Resources
### Dataset
A single stop sign image is used for this project. The image is available [here](https://static01.nyt.com/images/2011/12/11/magazine/11wmt1/mag-11WMT-t_CA0-jumbo.jpg), and in ImageNet, stop signs are considered 'street sign' class (class id 919).

Code Structure:

### 1: Adversarial Example Generation for ResNet-18
1. Load the ResNet-18 model and predict the label for the provided stop sign image.
2. Perform untargeted attacks with random perturbations and observe the impact on ResNet-18 predictions.
3. Implement untargeted and targeted attacks using Fast Gradient Method (FGM) and Projected Gradient Descent (PGD), respectively.

### 2: Neural Network Visualization
1. Visualize maximal activation of specific filters on the first and last convolutional layers of AlexNet.
2. Visualize saliency maps for the last convolutional layer of AlexNet given the stop sign input.

### 3: Evaluation of Probabilistic Robustness
1. Estimate the misclassification rate of ResNet-18 with random perturbations.
2. Compute and plot the relative error of the estimator.
3. Sample around an adversarial example, apply FGM attack, and estimate the misclassification rate.

## Reference
1. CMU 24784 Spring 2024 P1 Google Colab Notebook [Link](https://drive.google.com/file/d/1PM6f9J8Ozewmf4QdoUrsi57MxynlRHd-/view?usp=sharing)
2. TorchVision models [Link](https://pytorch.org/vision/0.8/models.html)
3. ScratchAI [Link](https://github.com/iArunava/scratchai)
4. FlashTorch [Link](https://github.com/MisaOgura/flashtorch)
5. MapExtrackt [Link](https://github.com/lewis-morris/mapextrackt)
