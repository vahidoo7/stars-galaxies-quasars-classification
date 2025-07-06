# stars-galaxies-quasars-classification
Code for semi-supervised classification of astronomical objects using K-means and Random Forest.

This project implements a semi-supervised classification framework combining K-means clustering and Random Forest to classify stars, galaxies, and quasars using limited labeled data.

Key Steps:

**1**- Clustering: The unlabeled dataset is partitioned into *K=50* clusters using K-means.

**2**- Label Propagation: Spectroscopic labels from cluster centroids are propagated to 95% of members (5% outliers excluded).

**3**- Classification: A Random Forest is trained on the expanded pseudo-labeled dataset.

Advantages:

✔ Label Efficiency: Achieves performance comparable to supervised methods using only 50 labeled samples.

✔ Robustness: Majority voting over 100 K-means initializations reduces instability.

✔ Scalability: Designed for high-dimensional photometric surveys (tested on 190 color features).
