# Filtered GAN Data Augmentation (FashionMNIST)

## Overview
This project explores how **GAN-generated synthetic data** can be used to improve performance on **imbalanced image classification** tasks. Using the **FashionMNIST** dataset, a target class is intentionally under-represented to simulate class imbalance. A **Generative Adversarial Network (GAN)** is then trained exclusively on the minority class to generate synthetic samples.

To ensure data quality, generated samples are **filtered using the discriminator’s realism score**, and only the most realistic synthetic images are retained for augmentation. A classifier is trained before and after augmentation to evaluate the impact on **minority-class accuracy**.

---

## Key Features
- **Imbalanced Dataset Construction:** Simulated class imbalance by downsampling a selected minority class (e.g., *Sneaker*).
- **GAN-Based Synthetic Generation:** Trained a generator–discriminator pair to model the minority-class data distribution.
- **Discriminator-Based Filtering:** Ranked generated samples using discriminator confidence and retained only high-quality synthetic images.
- **Quantitative Evaluation:** Compared baseline and augmented classifiers, achieving a minority-class accuracy improvement from **0.692 to 0.802**.

---

## Objectives
To demonstrate a practical and reproducible approach for addressing **class imbalance** using **filtered GAN-based data augmentation**, and to show how quality-controlled synthetic data can significantly improve minority-class performance without altering the core classification architecture.

---

## Results
- **Baseline Minority Accuracy:** 0.692  
- **Augmented Minority Accuracy:** 0.802  
- **Improvement:** +11.0 percentage points  

The results show that discriminator-filtered GAN augmentation provides a substantial benefit over naïve augmentation approaches.

---

## Notes
- Fully connected GANs were used to minimize architectural complexity.
- Generated samples exhibit limited diversity due to mode collapse, which is mitigated through filtering.
- The focus of evaluation is **minority-class accuracy**, not overall accuracy.

---
