# 🌍 EuroSAT Land Cover Classification: Processing & Recognition

![Project Status](https://img.shields.io/badge/Status-Completed-success)
![Course](https://img.shields.io/badge/Course-Image%20Processing-blue)
![Course](https://img.shields.io/badge/Course-Image%20Recognition-blue)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?logo=PyTorch&logoColor=white)
![Jupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?logo=jupyter&logoColor=white)

## Project Overview

This repository hosts a joint project for the **Image Processing** and **Image Recognition** courses. The study focuses on the complex classification of socio-economic land cover using the **EuroSAT (RGB)** satellite imagery dataset. 

The project implements a comprehensive and comparative analytical pipeline. It bridges fundamental classical image processing techniques (spatial and frequency domain analysis, handcrafted feature extraction) with state-of-the-art deep learning architectures (Convolutional Neural Networks). 

By evaluating these two paradigms side-by-side, we aim to demonstrate the evolutionary shift from mathematically rigid descriptors to dynamic representation learning in modern remote sensing.

---

## Team Members

* **Aleksandra Szpakowska**
* **Wojciech Hrycenko**

---

## Analytical Pipeline & Methodology

The project is structured into a logical, step-by-step Jupyter Notebook containing the following phases:

1. **Exploratory Data Analysis & Processing Lab:** * Spatial filtering (Bilateral, Gaussian, Canny Edge Detection, Morphology).
   * Frequency domain analysis using the 2D Fast Fourier Transform (FFT).
   * Contrast Limited Adaptive Histogram Equalization (CLAHE) and Otsu's Thresholding.
2. **Feature Engineering & Unsupervised Learning:** * Extraction of high-dimensional descriptors: **HOG** (geometry), **LBP** (texture), and **Color Histograms** (spectral).
   * Dimensionality reduction using **PCA** and exploratory clustering via **K-Means**.
3. **Track A: Classical Machine Learning (Baseline):** * Feature selection using Mutual Information.
   * Supervised classification using **Random Forest** and **Support Vector Classifier (SVC)**, achieving an optimized performance ceiling of 85%.
4. **Track B: Deep Learning (End-to-End Recognition):** * Processing raw pixels with dynamic Data Augmentation.
   * Transfer Learning via a fine-tuned **ResNet18** architecture.
   * Advanced training optimization including Weight Decay (L2), Dropout, and Learning Rate Scheduling (`StepLR`), achieving **97% accuracy**.

---

## Key Findings

* **The Semantic Limit of Classical Features:** While classical algorithms performed well on distinct geometric tasks, they fundamentally struggled to differentiate visually overlapping classes (e.g., distinguishing tarmac highways from rivers based purely on HOG gradients).
* **The Power of Spatial Context:** The Deep Learning approach (Track B) shattered the classical accuracy ceiling. By learning hierarchical spatial features directly from raw pixels, the CNN successfully resolved the semantic ambiguities that plagued the classical models.
* **Optimization Impact:** Implementing rigorous training dynamics and a structured Train/Validation/Test split proved essential in preventing overfitting and stabilizing the deep learning model at near-perfect classification capabilities.

---

## Assessment Requirements Fulfilled

* **Integration:** The project seamlessly merges the syllabi of both Image Processing (filters, FFT, manual feature extraction) and Image Recognition (PCA, ML models, CNNs).
* **Data:** Based on the robust EuroSAT dataset.
* **Format:** Delivered as a fully documented, highly structured, and visually cohesive Jupyter Notebook.
* **Focus:** * Clear scientific narrative justifying the transition from classical to deep learning.
    * Rigorous model validation (Cross-Validation, Hold-out sets).
    * Deep interpretation of results supported by classification reports and confusion matrices.
