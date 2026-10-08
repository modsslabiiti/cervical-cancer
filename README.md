# Cervical Cancer Classification with BF-AD-AP-ResNets (BF-AD-AP-ResNet50, BF-AD-AP-ResNet101, and BF-AD-AP-ResNet152)

\---

## Table of Contents

* [Overview](#overview)
* [How to RUN](#installation)
* [Dataset](#dataset)



\---

## Overview

### Objective:

This project aims to classify cervical cancer colposcopy images using two datasets IARC and AnnoCerv:

1. **Type classification** (Type 1, Type 2, Type 3) on IARC
2. **Category classification** (Category 1, Category 2, Category 3) on AnnoCerv

### Key Steps:

1. **Preprocessing:** Includes image augmentation and segmentation.
2. **Classification with BF-AD-AP-ResNets:**

   * **Model:**

     * Extract features from the intermediate convolution blocks of each ResNets pass them through the EuPea Attention Module and select the features using the Adaptive Pooling layer (BF-AD-AP-ResNets), and fused them.
     * Merge the features of each BF-AD-AP-ResNets.
     * Normalize the augmented features of training set using Min-max normalization and then using this trained scaler normalize augmented features of the test set.
     * Classify using SVM.

\---



## How to RUN

### Prerequisites Installation

Ensure the following are installed on your machine:

* Python (>= 3.8)
* OpenCV
* NumPy
* Matplotlib
* Pandas
* Scikit-learn
* TensorFlow (with Keras API)

\---

### Folder straucture



Root/

├── 1 IARC/

│   ├── Main-Manuscript-Experiments/

│   │   ├── 0-Preprocessing/

│   │   │   └── (Image preprocessing and augmentation code)

│   │   ├── 1-Experiments/

│   │   │   └── (Proposed BF-AD-AP-ResNet50/101/152 feature extraction,

│   │   │        fusion, Min-Max normalization, and classification code)

│   │   ├── 2-Model-Analysis/

│   │   │   └── (Statistical tests, AUC-PR values, calibration curves,

│   │   │        and confusion matrix code)

│   │   ├── 3-Ablation/

│   │   │   └── (Ablation study code analyzing contribution of each component)

│   │   └── 4-XAI/

│   │       └── (Explainability code using LIME and SHAP)

│   │

│   └── Appendix-Experiments/

│       ├── 1-Vision-Transformer/

│       │   └── (Experiments using Vision Transformer architecture)

│       ├── 2-MLP/

│       │   └── (Experiments using Multi-Layer Perceptron)

│       └── 3-Overestimated-Recordwise/

│           └── (Implementation on augmented/record-wise dataset —

│                results reported in appendix)

│

└── 2 AnnoCerv/

&#x20;   ├── Main-Manuscript-Experiments/

&#x20;   │   ├── 0-Preprocessing/

&#x20;   │   │   └── (Image preprocessing and augmentation code)

&#x20;   │   ├── 1-Experiments/

&#x20;   │   │   └── (Proposed BF-AD-AP-ResNet50/101/152 feature extraction,

&#x20;   │   │        fusion, Min-Max normalization, and classification code)

&#x20;   │   ├── 2-Model-Analysis/

&#x20;   │   │   └── (Statistical tests, AUC-PR values, calibration curves,

&#x20;   │   │        and confusion matrix code)

&#x20;   │   ├── 3-Ablation/

&#x20;   │   │   └── (Ablation study code analyzing contribution of each component)

&#x20;   │   └── 4-XAI/

&#x20;   │       └── (Explainability code using LIME and SHAP)

&#x20;   │

&#x20;   └── Appendix-Experiments/

&#x20;       ├── 1-Vision-Transformer/

&#x20;       │   └── (Experiments using Vision Transformer architecture)

&#x20;       ├── 2-MLP/

&#x20;       │   └── (Experiments using Multi-Layer Perceptron)

&#x20;       └── 3-Overestimated-Recordwise/

&#x20;           └── (Implementation on augmented/record-wise dataset —

&#x20;                results reported in appendix)







Dataset directory structure
├── Fold-wise
├── Fold-1
├── Training
├── Testing
├── Fold-2
├── Training
├── Testing
├── Fold-3
├── Training
├── Testing
├── Fold-4
├── Training
├── Testing
├── Fold-5
├── Training
├── Testing









### Run

Set the Path and run each cell of each respective notebooks available in folders.

