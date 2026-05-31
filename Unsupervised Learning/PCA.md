# Principal Component Analysis (PCA)

## Overview

Principal Component Analysis (PCA) is an unsupervised Machine Learning technique used for dimensionality reduction.

It reduces the number of features in a dataset while preserving as much important information as possible.

---

## What is PCA?

PCA transforms the original features into a new set of features called:

### Principal Components

These principal components capture the maximum variance present in the dataset.

👉 Simple idea:

"Keep the important information and remove unnecessary complexity."

---

## Why Do We Need PCA?

Real-world datasets often contain:

- Too many features
- Correlated variables
- Redundant information

These problems can:
- Increase training time
- Cause overfitting
- Make visualization difficult

PCA helps solve these issues.

---

## Dimensionality Reduction

Dimensionality Reduction means reducing the number of input features while retaining the most useful information.

Example:

Original Dataset:
- Age
- Salary
- Experience
- Education
- City
- Gender

After PCA:

- Principal Component 1
- Principal Component 2

The dataset becomes simpler while preserving most information.

---

## Key Concepts

### Variance

Variance measures how much data points spread out.

Higher variance means:
- More information
- More useful feature

PCA tries to preserve maximum variance.

---

### Principal Components

Principal Components are new features created from existing features.

- PC1 → captures maximum variance
- PC2 → captures second highest variance
- PC3 → captures third highest variance

And so on.

---

## How PCA Works

### Step 1: Standardize Data

All features are scaled to a similar range.

---

### Step 2: Compute Covariance Matrix

Relationships between features are calculated.

---

### Step 3: Calculate Eigenvalues and Eigenvectors

These determine:

- Important directions
- Amount of variance captured

---

### Step 4: Select Principal Components

Components with highest variance are chosen.

---

### Step 5: Transform Dataset

Data is projected onto selected principal components.

---

## Explained Variance

Explained Variance tells us how much information a principal component contains.

Example:

| Component | Variance Explained |
|------------|-------------------|
| PC1 | 70% |
| PC2 | 20% |
| PC3 | 10% |

Using PC1 and PC2 preserves:

70% + 20% = 90%

of the original information.

---

## Visual Representation

![PCA](../images/pca.png)

---

## Graph Explanation

- Original data may have many dimensions
- PCA projects data onto fewer dimensions
- Most information is retained
- Visualization becomes easier

---

## Python Implementation

```python
from sklearn.decomposition import PCA
from sklearn.datasets import load_iris

# Load dataset
iris = load_iris()

X = iris.data

# Apply PCA
pca = PCA(n_components=2)

X_pca = pca.fit_transform(X)

print("Original Shape:", X.shape)
print("Reduced Shape:", X_pca.shape)
```

---

## Advantages

- Reduces dimensionality
- Faster model training
- Reduces overfitting
- Removes redundancy
- Better visualization

---

## Limitations

- Some information is lost
- Hard to interpret principal components
- Sensitive to feature scaling

---

## Applications

- Data Visualization
- Image Compression
- Noise Reduction
- Feature Extraction
- Recommendation Systems

---

## Key Takeaway

PCA is one of the most widely used dimensionality reduction techniques that simplifies datasets while preserving the most important information.

It helps improve efficiency, visualization, and model performance.

---

