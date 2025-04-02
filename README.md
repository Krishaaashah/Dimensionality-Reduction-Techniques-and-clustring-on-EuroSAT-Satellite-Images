# 🌍 EuroSAT Dimensionality Reduction

This project applies multiple dimensionality reduction techniques to the **EuroSAT dataset** for efficient satellite imagery analysis.

## 📂 Dataset Overview
The **EuroSAT dataset** consists of satellite images categorized into various land use classes such as *Forest*, *Industrial*, *Residential*, and more. Each image has a resolution of `64x64` pixels with RGB color channels.

## 🔧 Applied Dimensionality Reduction Techniques
We implemented several dimensionality reduction techniques to analyze and visualize high-dimensional data:

- **📌 PCA (Principal Component Analysis)** – Reduces feature space while preserving maximum variance.
- **📌 LDA (Linear Discriminant Analysis)** – Projects data to maximize class separability.
- **📌 SVD (Singular Value Decomposition)** – Decomposes data into fundamental components.
- **📌 t-SNE (T-Distributed Stochastic Neighbor Embedding)** – Maps high-dimensional data into 2D/3D space for visualization.
- **📌 MDS (Multidimensional Scaling)** – Preserves pairwise distances for spatial similarity analysis.

## 🛠️ Installation & Requirements
Ensure you have Python installed along with the necessary libraries before running the scripts. Install the dependencies using:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
