# Fashion-MNIST Clustering Before and After PCA

## Project Overview

This project explores how dimensionality reduction using Principal Component Analysis (PCA) affects clustering performance on the Fashion-MNIST dataset.

We applied KMeans clustering before and after PCA and compared the results using the Silhouette Score and Adjusted Rand Index (ARI). We also explored different numbers of PCA components and compared KMeans with another clustering algorithm, DBSCAN.

## Dataset

- **Dataset:** Fashion-MNIST
- **Source:** [Kaggle – Fashion-MNIST](https://www.kaggle.com/datasets/zalando-research/fashionmnist)
- **Original size:** 60,000 images
- **Features:** 784 pixel values per image
- **Image dimensions:** 28 × 28 pixels
- **Classes:** 10 clothing categories

Each row represents one clothing image, with 784 pixel features and one label indicating its actual category.

## Project Objectives

- Explore and understand the Fashion-MNIST dataset.
- Prepare the data for clustering.
- Apply KMeans using the original 784 pixel features.
- Reduce dimensionality using PCA.
- Compare KMeans results before and after PCA.
- Evaluate clustering performance using Silhouette Score and ARI.
- Experiment with different numbers of PCA components.
- Compare KMeans with DBSCAN.

## Project Workflow

1. **Data Collection:** Download the Fashion-MNIST dataset from Kaggle.
2. **Data Cleaning:** Check missing values and remove duplicate rows.
3. **Data Exploration:** Explore the class distribution and visualize sample images.
4. **Data Preprocessing:** Separate features and labels, then apply StandardScaler.
5. **KMeans Before PCA:** Apply KMeans using all 784 pixel features.
6. **PCA:** Reduce the original features to two principal components.
7. **KMeans After PCA:** Apply KMeans again using the two PCA components.
8. **Evaluation:** Compare the clustering results using Silhouette Score and ARI.
9. **Bonus Experiments:** Test different PCA component counts and compare KMeans with DBSCAN.

## Main Results

| Metric | Before PCA | After PCA |
|---|---:|---:|
| Silhouette Score | 0.127 | 0.404 |
| ARI | 0.322 | 0.261 |

The Silhouette Score increased after PCA, indicating better separation between clusters in the reduced two-dimensional space.

However, the ARI decreased, meaning that the clusters became less aligned with the actual clothing categories.

This shows that better cluster separation does not necessarily mean better agreement with the true labels.

## Bonus Experiments

### 1. Different PCA Components

We tested different numbers of PCA components:

- 2 components
- 10 components
- 30 components
- 50 components

We compared the Silhouette Score, ARI, and explained variance for each experiment.

### 2. KMeans vs DBSCAN

We used DBSCAN as an alternative clustering algorithm and compared it with KMeans using the same ten-component PCA representation.

The comparison included the number of clusters, ARI, and Silhouette Score.

## Technologies and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- KaggleHub
- Jupyter Notebook / Google Colab

## How to Run the Project

1. Clone or download this repository.
2. Install the required libraries:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn kagglehub
   ```

3. Open `Fashion-MNIST_Clustering_Before_and_After_PCA.ipynb` using Jupyter Notebook or Google Colab.
4. Run the notebook cells in order.
5. Make sure you have an internet connection so KaggleHub can download the dataset.

## Team

| Name | GitHub |
|---|---|
| Fahad Al-Nahi | [@Skkinner](https://github.com/Skkinner) |
| Basma Almuntaser | [@Basmaalmuntaser](https://github.com/Basmaalmuntaser) |
| Raghad Alharbi | [@Raghad5MH](https://github.com/Raghad5MH) |
| Reham | [@YOUR_USERNAME](https://github.com/YOUR_USERNAME) |

## Acknowledgments

- Dataset: [Fashion-MNIST – Zalando Research](https://www.kaggle.com/datasets/zalando-research/fashionmnist)
- Scikit-learn documentation: [https://scikit-learn.org/](https://scikit-learn.org/)
- PCA documentation: [https://scikit-learn.org/stable/modules/decomposition.html#pca](https://scikit-learn.org/stable/modules/decomposition.html#pca)
- Clustering documentation: [https://scikit-learn.org/stable/modules/clustering.html](https://scikit-learn.org/stable/modules/clustering.html)
