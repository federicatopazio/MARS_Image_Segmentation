# Artificial Neural Networks and Deep Learning HW2 - AY 2024/2025

## Challenge: Mars Terrain Segmentation

This challenge involved segmenting Mars terrain images into five classes: **Background, Soil, Bedrock, Sand, and Big Rocks**. We built a deep learning model from scratch, optimizing it for the **Mean Intersection over Union (MeanIOU) metric**.

## Data & Augmentation

Dataset: **2,615** images, with **110** low-quality images removed. Maintaining the original class distribution provided the best results.

Key augmentations:
- Horizontal & vertical flips
- Exclusion of rotations & zoom to preserve features

**Performance Boost:** Flipping-based augmentation improved MeanIOU by **1%-6%**.

## Models & Training

**Best Model:** Multipath UNet with:
- **Multi-path encoders** (Convolutional, Residual, Global Context, Multiscale)
- **Squeeze-and-Excitation bottleneck** for feature fusion
- **Focal Loss** with class balancing

**Hyperparameter Tuning:**
- **Optuna-based optimization** for learning rate, batch size
- **Best optimizer:** AdamW with weight decay

**Final Results:** MeanIOU **0.74** (Best Submission)

## More Info

Refer to the [report](report.pdf) and [notebooks](/notebooks).

## Team
* [Mattia Piccinato](https://github.com/peetceenatoo)
* [Matteo Salari](https://github.com/matteo-salari)
* [Davide Salonico](https://github.com/DavideSalonico)
* [Federica Topazio](https://github.com/federicatopazio)
