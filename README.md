# PCA-Based Eigenface Recognition

## Introduction
This project implements **Principal Component Analysis (PCA)** for dimensionality reduction in face images, creating **Eigenfaces** that represent significant facial features. PCA is a powerful linear technique used to reduce high-dimensional data while retaining essential information.

## Concept Overview
Face recognition often deals with high-dimensional data (e.g., 256×256 pixel images). PCA helps by:
- Computing a lower-dimensional representation of faces.
- Identifying key facial features (Eigenfaces).
- Reconstructing faces using a subset of Eigenfaces.
- Analyzing reconstruction error across different numbers of Eigenfaces (K).

## Dataset
- The dataset contains **177 grayscale face images** of size **256×256 pixels**.
- The first **157 images** are used for training, and the remaining **20 images** for testing.
- Each image is reshaped into a **1D vector** before applying PCA.

## Implementation Details
### 1. **Preprocessing**
- Convert images to grayscale.
- Reshape images into a **data matrix** (rows = faces, columns = pixels).
- Compute the **mean face** and center the data.

### 2. **PCA Computation**
- Use **Singular Value Decomposition (SVD)** to compute eigenfaces.
- Select the top **K Eigenfaces** to reduce dimensionality.
- Visualize the top **10 Eigenfaces**.

### 3. **Face Reconstruction**
- Project test images onto the Eigenface space.
- Reconstruct images using selected **K Eigenfaces**.
- Compare original vs. reconstructed faces.

### 4. **Reconstruction Error Analysis**
- Compute the reconstruction error:
  \[ \frac{||\hat{Y} - Y||^2}{N} \]
- Test with different values of **K** (10, 30, 50, 100, 150).
- Plot error vs. number of Eigenfaces.

## Results
- **Visualization of Top 10 Eigenfaces**
- **Reconstructed images vs. original test images**
- **Reconstruction error plot** for different values of K.

## Key Learnings
- PCA is effective in reducing dimensionality while retaining essential information.
- Eigenfaces provide a way to analyze facial features mathematically.
- Increasing K improves reconstruction but increases computation.


