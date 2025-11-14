# MSCS_634_Lab3
## Overview
This lab focuses on applying clustering techniques to the Wine dataset from the sklearn library. The goal is to explore how K-Means and K-Medoids behave on the same dataset, compare their performance, and visualize the differences in how each algorithm groups the samples. By analyzing the resulting clusters and evaluation metrics, the lab provides a deeper understanding of how clustering methods interpret structure in real-world data.

## Purpose of the Lab
The purpose of this lab is to:
- Load, prepare, and standardize the Wine dataset.
- Apply two clustering algorithms: K-Means and K-Medoids using three clusters.
- Evaluate clustering quality using the Silhouette Score and Adjusted Rand Index (ARI).
- Visualize the differences in cluster assignments and cluster centers.
- Compare how each algorithm handles cluster structure, center placement, and boundary decisions.

## Key Insights from the Clustering Results
- K-Means produced smoother and more spherical clusters, which aligns with how it computes centroids as the mean of all points. The cluster centers appeared well-positioned at the center of each group.
- K-Medoids created slightly less symmetric clusters, since medoids must be actual data points. This made the cluster centers appear slightly off-center in the plots, but it also made the algorithm more robust to noise and potential outliers.
- Several points near cluster boundaries were assigned differently between the two algorithms. These differences highlight how K-Means optimizes for overall variance, while K-Medoids is more conservative and focuses on minimizing dissimilarity around real data points.

## Challenges and Decisions Made
The main challenge encountered during the lab was a ModuleNotFoundError when trying to import the `KMedoids` class from `sklearn_extra.cluster`. This occurred because the `sklearn-extra` package was not pre-installed in the environment. The issue was addressed by installing the package manually before running the K-Medoids portion of the lab. After installation, the clustering and visualizations worked as expected.

Other than that, the preprocessing, clustering steps, and visual analysis were straight forward
