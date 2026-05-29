# K-Means Clustering

## Overview

K-Means Clustering is an unsupervised Machine Learning algorithm used to group similar data points into clusters.

It divides the dataset into K different clusters based on similarity.

---

## What is Clustering?

Clustering means grouping similar data points together.

👉 Simple idea:

"Similar data points belong to the same group."

---

## What is K in K-Means?

K represents the number of clusters.

Example:
- K = 2 → data divided into 2 clusters
- K = 3 → data divided into 3 clusters

---

## How K-Means Works

### Step 1: Choose Number of Clusters (K)

The user selects the number of clusters.

---

### Step 2: Initialize Centroids

Random points are selected as cluster centers.

These centers are called:
- Centroids

---

### Step 3: Assign Data Points

Each data point is assigned to the nearest centroid.

---

### Step 4: Update Centroids

The centroid position is recalculated using the mean of all assigned points.

---

### Step 5: Repeat

Steps 3 and 4 continue until centroids stop changing.

---

## Centroid

A centroid is the center point of a cluster.

It represents the average position of all points in that cluster.

---

## Visual Representation

![KMeans](../images/kmeans.png)

---

## Graph Explanation

- Different colored points represent different clusters  
- Centroids represent cluster centers  
- Nearby points belong to the same cluster  

---

## Elbow Method

The Elbow Method helps determine the optimal value of K.

The graph plots:
- Number of clusters (K)
- WCSS (Within Cluster Sum of Squares)

The "elbow point" is considered the best K value.

---

## Python Implementation

```python
from sklearn.cluster import KMeans
import numpy as np

# Sample data
X = np.array([
    [1, 2],
    [1, 4],
    [1, 0],
    [10, 2],
    [10, 4],
    [10, 0]
])

# Model
kmeans = KMeans(n_clusters=2)

# Train
kmeans.fit(X)

# Cluster labels
print(kmeans.labels_)

# Centroids
print(kmeans.cluster_centers_)
```

---

## Advantages

- Simple and easy to understand  
- Fast and efficient  
- Works well for large datasets  

---

## Limitations

- Choosing K is difficult  
- Sensitive to outliers  
- Different initial centroids may give different results  

---

## Applications

- Customer Segmentation  
- Image Compression  
- Recommendation Systems  
- Pattern Recognition  

---

## Key Takeaway

K-Means is one of the most popular clustering algorithms used to group similar data points together based on distance and similarity.

---

