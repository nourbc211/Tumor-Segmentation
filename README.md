#  Brain Tumor Segmentation 

This project focuses on **brain tumor segmentation** using deep learning models, with an emphasis on **generalization** across datasets. We benchmark different U-Net-based architectures on **BraTS 2020** and a **Kaggle LGG MRI segmentation dataset**, and evaluate their performance using metrics like **Dice coefficient** and **Intersection over Union (IoU)**.

## Datasets

We use two main datasets:

- **BraTS 2020**: Multimodal brain MRI scans (T1, T1ce, T2, FLAIR) with pixel-wise tumor annotations.
- **Kaggle LGG**: Lower Grade Glioma MRI dataset with annotated tumor regions in axial slices.

## Models

We implement and compare the following segmentation models:

- **U-Net** : as a baseline model
- **Attention U-Net**
- **U-Net with **ResNet** and **EfficientNet** encoders.

## Evaluation Metrics

We use the following metrics for evaluation:

- **Dice Coefficient (F1 Score)** – overlap between predicted and ground truth masks
- **Intersection over Union (IoU)** – ratio of intersection to union of predicted and ground truth

## Cross-Dataset Generalization

We explore how models trained on BraTS perform on LGG (and vice versa). Key experiments include:

- Classical trainin and validation on one dataset
- Training on BraTS, evaluating on LGG
- Fine-tuning on LGG after BraTS pretraining
- Comparing performance with and without domain-specific augmentation

## Code

- **tumor_segmentation_UNET.ipynb** : Notebook containing the baseline model and its results.
- **tumor_segmentation_Res_Efficient_Attention** : Contains the variants of U-Net and their result.
