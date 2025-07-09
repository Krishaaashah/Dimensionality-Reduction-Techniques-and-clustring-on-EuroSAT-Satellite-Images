# 🌍 EuroSAT Image Analysis with Dimensionality Reduction and Clustering

This project explores the **EuroSAT dataset**, applying both **dimensionality reduction techniques** and **unsupervised clustering algorithms** to analyze satellite images categorized by land use and land cover types. The goal is to reduce data complexity, extract meaningful features, and identify natural groupings of images.

---

## 📁 Dataset Description

- **Dataset**: [EuroSAT](https://zenodo.org/record/7711810)
- **Images**: ~27,000 RGB satellite images
- **Resolution**: 64×64 pixels
- **Classes**: 10 land use categories (e.g., Forest, SeaLake, Residential, Industrial, etc.)
- **Source**: Sentinel-2 satellite imagery

---

##  Objectives

- Preprocess and flatten satellite image data for analysis
- Apply dimensionality reduction techniques to simplify data while preserving information
- Use clustering algorithms to group similar images without using class labels
- Evaluate clustering performance using robust metrics

---

##  Dimensionality Reduction Techniques

To reduce computational overhead and enhance visualization, the following techniques were applied:

###  Principal Component Analysis (PCA)
- Retained most variance while reducing dimensionality
- Helped speed up clustering and modeling tasks
- ![image](https://github.com/user-attachments/assets/632f2f4e-7381-4fef-bfac-45ee73f2cdeb)


###  Linear Discriminant Analysis (LDA)
- Supervised technique used to maximize class separability
- Applied only when true labels were available for evaluation
- ![image](https://github.com/user-attachments/assets/18bdd9b3-bf12-4038-8f97-5e264729ba62)


###  Truncated SVD
- Matrix factorization approach useful for sparse image data
- Alternative to PCA without centering

###  t-SNE
- Visualized high-dimensional data in 2D
- Showed clear separation in local clusters (not used for modeling)
- ![image](https://github.com/user-attachments/assets/5bcf64ac-ff9f-4770-9195-b807c96ef21b)


###  MDS
- Preserved distance relationships between data points
- Useful for visual interpretation
- ![image](https://github.com/user-attachments/assets/a88430bc-bce0-4f45-bc45-c743d04369b5)

### Comparsion
- ![image](https://github.com/user-attachments/assets/1727da21-f84f-4b12-b71c-f936fcb63520)



---

##  Clustering Techniques

The following unsupervised learning methods were used to group images based on visual similarity:

###  K-Means Clustering
- Partitioned data into K clusters based on distance to cluster centroids
- Optimal K selected using **Elbow Method** and **Silhouette Score**
- ![image](https://github.com/user-attachments/assets/38b76c65-a47d-42c3-94bc-50c2e53f9a2d)


###  Agglomerative Clustering
- Hierarchical clustering algorithm using a bottom-up approach
- Dendrogram not plotted due to size, but clustering comparison was conducted
- ![image](https://github.com/user-attachments/assets/e1efc26f-0652-4c27-ba53-f2ffbad55f46)


---

##  Performance Evaluation Metrics

Each clustering technique was evaluated using the following metrics:

| Metric | Description | Ideal |
|--------|-------------|-------|
| **Silhouette Score** | Measures cohesion/separation | Closer to 1 |
| **Davies–Bouldin Index** | Average similarity of clusters | Closer to 0 |
| **Calinski–Harabasz Index** | Ratio of between-cluster to within-cluster dispersion | Higher is better |
| **Adjusted Rand Index** | Compares clustering to true labels (supervised) | Closer to 1 |

- ![image](https://github.com/user-attachments/assets/624c7818-1748-489d-aad9-c2fcb9105b65)


---

##  Tools & Libraries

- **Python 3.10**
- **NumPy, Pandas** – Data handling
- **Scikit-learn** – Dimensionality reduction, clustering, evaluation metrics
- **Matplotlib, Seaborn** – Visualization
- **Keras** – Image preprocessing
- **Jupyter Notebook** – Interactive development

---

##  Conclusion

This project demonstrates how combining dimensionality reduction with clustering can reveal meaningful structure in satellite image data. Both K-Means and Agglomerative clustering effectively grouped similar images, and evaluation metrics provided insights into their quality. Such techniques offer scalable and label-free solutions for remote sensing analysis.

---
.

