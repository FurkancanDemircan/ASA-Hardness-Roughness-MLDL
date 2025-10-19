# Hardness and Surface Roughness Prediction of 3D-Printed ASA Components Using Machine Learning and Deep Learning
This repository contains the dataset, source code, and experimental results for the study:

**“Hardness and Surface Roughness of 3D-printed ASA Components Subjected to Acetone Vapor Treatment and Different Production Variables: A Multi-estimation Work via Machine Learning and Deep Learning.”**
The project investigates how **layer thickness**, **infill rate**, and **acetone vapor treatment time** affect two important surface quality characteristics of **3D-printed Acrylonitrile Styrene Acrylate (ASA)** components:

- **Shore-D Hardness**
- **Surface Roughness (Ra)**

Using a combination of **experimental measurements**, **machine learning (ML)**, and **deep learning (DL)** models, the study evaluates multiple prediction strategies and proposes a hybrid approach. A **1D-CNN–SVR model** achieves the best performance, enabling **simultaneous multi-target prediction** of hardness and roughness from process parameters alone.

---

## Dataset

- Format: `hardness_roughness.xlsx`
- Total observations: **108**
- Inputs: `Layer Thickness`, `Infill Rate`, `Vaporizing Duration`
- Outputs: `Hardness (Shore D)`, `Surface Roughness (µm)`
- DOI: **https://doi.org/10.5281/zenodo.17390033**

The dataset includes experimental hardness measurements (ASTM D2240-15) and profilometer-based surface roughness values.

---

## Models and Findings

The following ML/DL methods were evaluated:

| Category | Models |
|----------|--------|
| ML | RF, GB, XGBoost, SVR, KNN, ET, Bagging, Stacking, Ridge, LR |
| DL | 1D-CNN, 2D-CNN, RNN, LSTM |
| Hybrid | **1D-CNN Feature Extraction + SVR** ✅ (Best) |

**Best Results (5-fold cross-validation):**

- **R² = 0.9614**
- **MSE = 2.0941**

The hybrid 1D-CNN + SVR approach outperformed all standalone ML and DL models.

---
