# Food-101 CNN vs Transformer Model Comparison

## Project Title
Comparative Performance Analysis of ResNet50, ViT-B/16, and Swin Transformer Tiny on Food Image Classification

## Course
Generative Modeling

## Student
Muhammad Ramzan  
M.Phil Artificial Intelligence  
PUCIT, University of the Punjab

---

## Project Overview

This project compares the performance of three deep learning models for image classification:

- ResNet50
- Vision Transformer (ViT-B/16)
- Swin Transformer Tiny

All models were trained and evaluated on the same Food-101 Small dataset using transfer learning.

---

## Dataset

Dataset: Food-101 Small: 10 Categories Train/Val/Test Split

Classes:
- chicken_curry
- chocolate_cake
- fish_and_chips
- hamburger
- ice_cream
- pad_thai
- pizza
- ramen
- sushi
- tacos

Dataset split:

| Split | Images |
|---|---:|
| Train | 2400 |
| Validation | 300 |
| Test | 300 |

---

## Experimental Setup

| Setting | Value |
|---|---|
| Image Size | 224 × 224 |
| Optimizer | AdamW |
| Learning Rate | 1e-4 |
| Loss Function | CrossEntropyLoss |
| Epochs | 10 |
| Hardware | Google Colab Tesla T4 GPU |
| Framework | PyTorch |

---

## Models

### ResNet50
A CNN-based model using residual connections.

### ViT-B/16
A Vision Transformer model that divides images into patches and applies self-attention.

### Swin Transformer Tiny
A hierarchical transformer model using shifted window-based attention.

---

## Results

| Model | Validation Accuracy | Test Accuracy | Training Time | Parameters |
|---|---:|---:|---:|---:|
| ResNet50 | 91.67% | 93.00% | ~5 min | 23.5M |
| ViT-B/16 | 90.67% | 94.00% | ~17 min | 85.8M |
| Swin Transformer Tiny | 95.33% | 92.67% | ~6.5 min | 27.5M |

---

## Key Findings

- ViT-B/16 achieved the highest test accuracy.
- ResNet50 was the fastest model.
- Swin Transformer Tiny achieved the highest validation accuracy and showed stable training behavior.
- Most classification errors occurred between visually similar food classes.

---

## Conclusion

ResNet50 provides fast and reliable performance. ViT-B/16 achieves the highest test accuracy but requires more computation. Swin Transformer Tiny offers the best balance between efficiency, accuracy, and generalization.

---

## Tools Used

- Python
- PyTorch
- Torchvision
- Google Colab
- Kaggle Dataset
- Matplotlib
- Scikit-learn
- Seaborn

---

## Repository Structure

```text
notebooks/
  01_ResNet50_Assignment3.ipynb
  02_ViT_B16_Assignment3.ipynb
  03_Swin_Tiny_Assignment3.ipynb

plots/
  training_curves/
  confusion_matrices/

report/
  Assignment3_Report.pdf

README.md
requirements.txt
