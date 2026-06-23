# Skin Disease Classification and Segmentation

## Overview

This repository contains three deep learning experiments focused on skin disease analysis using computer vision techniques:

1. **SkinDiseaseClassification** – Skin disease classification using ResNet-18.
2. **Augmented** – Analysis of brightness augmentation and its impact on model robustness.
3. **Segmentation** – Skin lesion segmentation using U-Net.

---

## Prerequisites

### Kaggle API Setup

The datasets used in this project are downloaded directly from Kaggle using the Kaggle API.

1. Create a Kaggle account.
2. Navigate to **Account → API → Create New API Token**.
3. Download the `kaggle.json` file.
4. Place the file in the appropriate Kaggle configuration directory.

For Windows:

```bash
C:\Users\<username>\.kaggle\kaggle.json
```

Install Kaggle:

```bash
pip install kaggle
```

You can then download datasets directly from the notebook using Kaggle API commands.

---

# 1. SkinDiseaseClassification

## Objective

The goal of this experiment is to classify different skin diseases using a deep learning model based on **ResNet-18**.

## Methodology

* Dataset downloaded from Kaggle.
* Images resized and preprocessed.
* Transfer learning performed using a pretrained ResNet-18 model.
* Final classification layer modified for skin disease categories.
* Model trained and evaluated on validation data.

## Additional Experiment

To study real-world robustness, the trained model was tested on images with different brightness levels.

Brightness factors evaluated include:

* Darkened images
* Original images
* Brightened images

The objective was to analyze how lighting conditions affect classification performance.

---

# 2. Augmented

## Objective

This experiment investigates whether training with brightness-augmented images improves model robustness.

## Methodology

* Multiple brightness variations were generated from the original dataset.
* A new ResNet-18 model was trained using the augmented dataset.
* The model was evaluated on images with different brightness levels.

## Comparison Study

Performance of:

* Original ResNet-18 model
* Brightness-Augmented ResNet-18 model

was compared across multiple brightness conditions.

This experiment demonstrates how data augmentation can improve generalization and robustness against varying lighting environments.

---

# 3. Segmentation

## Objective

The goal of this experiment is to identify and segment lesion regions from skin images.

## Model Architecture

* U-Net Architecture
* Encoder-Decoder structure
* Pixel-level lesion segmentation

## Methodology

* Skin lesion images and corresponding masks were used.
* Images were preprocessed and resized.
* U-Net was trained to predict lesion boundaries.
* Segmentation performance was evaluated using appropriate metrics.

## Applications

* Lesion localization
* Medical image analysis
* Preprocessing for classification systems
* Computer-aided diagnosis systems

---

## Technologies Used

* Python
* PyTorch
* Torchvision
* OpenCV
* sklearn
* NumPy
* Matplotlib
* Kaggle API
* seaborn

---

## Results

This repository explores both classification and segmentation approaches for skin disease analysis:

* Skin Disease Classification using ResNet-18
* Robustness Analysis under Brightness Variations
* Brightness Augmentation Study
* Skin Lesion Segmentation using U-Net

These experiments demonstrate the importance of data augmentation and segmentation techniques in improving the reliability of deep learning systems for medical image analysis.
