# PCA — Formative Assignment

This notebook implements Principal Component Analysis (PCA) from scratch
using NumPy and Matplotlib, applied to an Africanized fruit dataset (IITA, Cameroon)
containing 47 fruit records with measurements such as length, diameter,
weight, and seed count.

## What the notebook does
1. Loads the dataset and standardizes the numerical features (mean 0, std 1)
2. Computes the covariance matrix to capture relationships between features
3. Performs eigendecomposition (`np.linalg.eigh`) to find eigenvalues and eigenvectors
4. Sorts principal components by explained variance
5. Dynamically selects the number of components using a 90% cumulative
   variance threshold (2 components retained, ~94% of variance)
6. Projects the data onto the selected components (5D → 2D)
7. Visualizes the data before and after PCA with matplotlib
8. Includes an optimized, vectorized PCA function that scales to large datasets

## Requirements
- Python 3, NumPy (matplotlib for visualization only)

## Notes
- Rows with missing values are excluded before computing covariance
- PC1 mainly captures fruit size (length, diameter, weight); PC2 captures seed count