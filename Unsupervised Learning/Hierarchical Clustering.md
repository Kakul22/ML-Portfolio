# Hierarchical Clustering

## Overview

Hierarchical Clustering is an unsupervised Machine Learning algorithm used to group similar data points into clusters.

Unlike K-Means, it does not require specifying the number of clusters initially.

---

## What is Hierarchical Clustering?

Hierarchical Clustering builds a hierarchy of clusters.

👉 Simple idea:

"Start by considering each data point as a separate cluster and keep merging similar clusters."

---

## Types of Hierarchical Clustering

### Agglomerative Clustering

Bottom-Up Approach

- Each data point starts as its own cluster
- Closest clusters are merged repeatedly
- Process continues until one cluster remains

Most commonly used approach.

---

### Divisive Clustering

Top-Down Approach

- All data points start in one cluster
- Cluster is repeatedly divided into smaller clusters

Less commonly used.

---

## How Agglomerative Clustering Works

### Step 1

Treat each data point as a separate cluster.

---

### Step 2

Calculate distances between clusters.

---

### Step 3

Merge the closest clusters.

---

### Step 4

Repeat until all points belong to a single hierarchy.

---

## Distance Metrics

Common distance measures:

- Euclidean Distance
- Manhattan Distance
- Cosine Distance

---

## Linkage Methods

### Single Linkage

Uses minimum distance between clusters.

---

### Complete Linkage

Uses maximum distance between clusters.

---

### Average Linkage

Uses average distance between clusters.

---

### Ward Linkage

Minimizes variance within clusters.

Most commonly used.

---

## Dendrogram

A Dendrogram is a tree-like diagram used to visualize hierarchical clustering.

It helps determine the optimal number of clusters.

---

## Visual Representation

![Hierarchical Clustering](../images/hierarchical_clustering.png)

---

## Graph Explanation

- Each leaf represents a data point
- Branches represent cluster merges
- Height indicates distance between clusters
- Cutting the dendrogram at a specific height gives clusters

---

## Python Implementation

```python
from sklearn.cluster import AgglomerativeClustering
import numpy as np

X = np.array([
    [1, 2],
    [1, 4],
    [1, 0],
    [10, 2],
    [10, 4],
    [10, 0]
])

model = AgglomerativeClustering(n_clusters=2)

labels = model.fit_predict(X)

print(labels)
```

---

## Advantages

- No need to specify K initially
- Produces a hierarchy of clusters
- Easy to visualize using dendrograms

---

## Limitations

- Computationally expensive
- Not suitable for very large datasets
- Difficult to undo cluster merges

---

## Applications

- Customer Segmentation
- Gene Sequence Analysis
- Social Network Analysis
- Document Clustering

---

## Key Takeaway

Hierarchical Clustering creates a hierarchy of clusters and provides a flexible way to explore relationships between data points without predefining the number of clusters.

---

## Folder Structure

```text
Unsupervised_Learning/
│
├── Hierarchical_Clustering.md
```

---

## Markdown Image Code

```md
![Hierarchical Clustering](../images/hierarchical_clustering.png)
```
