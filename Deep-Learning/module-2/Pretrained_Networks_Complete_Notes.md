# Module 2 -- Topic 2.1.4

# Pre-trained Networks (Complete Notes)

> **Course:** MCA Semester III -- Deep Learning\
> **Module:** Module 2 -- Convolutional Neural Networks and GPU
> Accelerated Training\
> **Topic:** 2.1.4 Pre-trained Networks

------------------------------------------------------------------------

# Learning Objectives

After completing this topic, you will be able to:

-   Understand what a Pre-trained Network is.
-   Explain why Pre-trained Networks are used.
-   Understand Transfer Learning and Fine-Tuning.
-   Identify popular pre-trained models.
-   Explain industry applications.

------------------------------------------------------------------------

# Why Do We Need Pre-trained Networks?

Training a Deep Learning model from scratch requires:

-   Millions of images
-   Powerful GPUs
-   Huge training time
-   High computational cost

To avoid repeating the same work, researchers created **Pre-trained
Networks**.

------------------------------------------------------------------------

# What is a Pre-trained Network?

**Definition**

A Pre-trained Network is a neural network that has already been trained
on a very large dataset and can be reused for new tasks.

**Simple Meaning**

Instead of training a new model from the beginning, we use an already
trained model and adapt it to our problem.

------------------------------------------------------------------------

# Transfer Learning

**Definition**

Transfer Learning is the process of using knowledge learned from one
task to solve another related task.

Example:

ImageNet-trained model → Medical image classification.

------------------------------------------------------------------------

# Fine-Tuning

Fine-Tuning means training some or all layers of a pre-trained model on
a new dataset to improve performance.

------------------------------------------------------------------------

# Workflow

``` text
Large Dataset (ImageNet)
        │
        ▼
Pre-trained Model
        │
        ▼
Replace Final Layer
        │
        ▼
Train on New Dataset
        │
        ▼
New AI Model
```

------------------------------------------------------------------------

# Ways to Use a Pre-trained Model

## 1. Feature Extraction

-   Freeze earlier layers.
-   Train only the final classification layer.

## 2. Fine-Tuning

-   Retrain some or all layers.
-   Higher accuracy but more computation.

------------------------------------------------------------------------

# Popular Pre-trained Models

## LeNet

-   Early CNN model.
-   Handwritten digit recognition.

## AlexNet

-   Winner of ImageNet 2012.
-   Made CNNs popular.

## VGG16 / VGG19

-   Deep and simple architecture.
-   Widely used for learning and transfer learning.

## ResNet

-   Introduced skip connections.
-   Very deep and highly accurate.

## Inception (GoogLeNet)

-   Efficient architecture with multiple filter sizes.

## MobileNet

-   Lightweight.
-   Designed for mobile and embedded devices.

------------------------------------------------------------------------

# PyTorch Example

``` python
import torchvision.models as models

model = models.resnet50(pretrained=True)
```

------------------------------------------------------------------------

# Industry Applications

-   Google Photos
-   Google Lens
-   Apple Face ID
-   Tesla Self-Driving
-   Medical Diagnosis
-   Product Recognition
-   OCR Systems

------------------------------------------------------------------------

# Advantages

-   Saves training time.
-   Requires less data.
-   Better starting accuracy.
-   Lower computational cost.

------------------------------------------------------------------------

# Limitations

-   May not perfectly fit every dataset.
-   Large models require more memory.
-   Fine-tuning can still require GPUs.

------------------------------------------------------------------------

# Training from Scratch vs Pre-trained Model

  Training from Scratch   Pre-trained Model
  ----------------------- -------------------------------
  Starts from zero        Starts with learned knowledge
  Needs huge dataset      Works with smaller dataset
  Slow                    Fast
  Expensive               Cost-effective

------------------------------------------------------------------------

# Important Keywords

-   Pre-trained Network
-   Transfer Learning
-   Fine-Tuning
-   ImageNet
-   ResNet
-   VGG
-   AlexNet
-   MobileNet

------------------------------------------------------------------------

# One-Line Definitions

-   **Pre-trained Network:** A model already trained on a large dataset.
-   **Transfer Learning:** Reusing learned knowledge for a new task.
-   **Fine-Tuning:** Further training a pre-trained model.

------------------------------------------------------------------------

# Quick Revision

-   Pre-trained models are already trained.
-   Transfer Learning reuses learned knowledge.
-   Fine-Tuning improves performance on a new dataset.
-   Popular models include AlexNet, VGG, ResNet and MobileNet.

------------------------------------------------------------------------

# Exam Preparation

## 2 Marks

1.  Define Pre-trained Network.
2.  What is Transfer Learning?
3.  What is Fine-Tuning?
4.  Name any two pre-trained models.

## 5 Marks

1.  Explain Pre-trained Networks.
2.  Explain Transfer Learning with an example.
3.  Differentiate training from scratch and pre-trained models.

## 10 Marks

Explain Pre-trained Networks, Transfer Learning, Fine-Tuning,
advantages, limitations and applications.

------------------------------------------------------------------------

# University Answer Writing Tips

1.  Define the concept.
2.  Explain why it is needed.
3.  Draw the workflow diagram.
4.  Explain Transfer Learning and Fine-Tuning.
5.  Mention famous models and applications.
6.  Conclude with advantages.

------------------------------------------------------------------------

# Practice MCQs

## Easy

### Q1. A Pre-trained Network is:

A. Untrained model

B. Already trained model

C. Database

D. GPU

**Answer:** B

**Explanation:** It has already been trained on a large dataset.

------------------------------------------------------------------------

### Q2. Transfer Learning means:

A. Reusing learned knowledge

B. Compressing images

C. Deleting layers

D. Increasing epochs

**Answer:** A

**Explanation:** Knowledge from one task is reused for another.

------------------------------------------------------------------------

### Q3. Which dataset is commonly used for pre-training?

A. MNIST

B. ImageNet

C. Iris

D. CIFAR-10

**Answer:** B

**Explanation:** Many famous CNN models are trained on ImageNet.

------------------------------------------------------------------------

### Q4. Which model is designed for mobile devices?

A. AlexNet

B. ResNet

C. MobileNet

D. LeNet

**Answer:** C

**Explanation:** MobileNet is lightweight and optimized for mobile
hardware.

------------------------------------------------------------------------

## Medium

### Q5. Fine-Tuning means:

A. Further training a pre-trained model

B. Deleting layers

C. Removing data

D. Compressing images

**Answer:** A

------------------------------------------------------------------------

### Q6. Which PyTorch package provides pre-trained models?

A. torchvision.models

B. torch.optim

C. torch.cuda

D. torch.utils

**Answer:** A

------------------------------------------------------------------------

### Q7. An advantage of pre-trained models is:

A. Faster training

B. Less data requirement

C. Better starting accuracy

D. All of the above

**Answer:** D

------------------------------------------------------------------------

## Advanced

### Q8. Which model won the ImageNet 2012 competition?

A. LeNet

B. AlexNet

C. ResNet

D. VGG

**Answer:** B

------------------------------------------------------------------------

### Q9. Which model introduced skip connections?

A. VGG

B. AlexNet

C. ResNet

D. MobileNet

**Answer:** C

------------------------------------------------------------------------

### Q10. Which statement is correct?

A. Every model must be trained from scratch.

B. Transfer Learning adapts existing knowledge to new tasks.

C. Fine-Tuning is performed before pre-training.

D. MobileNet is the largest CNN model.

**Answer:** B

------------------------------------------------------------------------

# Final Summary

Pre-trained Networks are already trained deep learning models that save
time, computation and data. Using Transfer Learning and Fine-Tuning,
they can quickly solve new tasks with high accuracy. Popular examples
include AlexNet, VGG, ResNet and MobileNet.
