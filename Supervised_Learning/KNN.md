# K-Nearest Neighbors (KNN)

## Overview

K-Nearest Neighbors (KNN) is a supervised Machine Learning algorithm used for both classification and regression tasks.

It predicts the output of a new data point based on the nearest data points present in the dataset.

---

## What is KNN?

KNN works on the idea that:

"Similar data points are likely to belong to the same category."

The algorithm finds the nearest neighbors of a data point and makes predictions using those neighbors.

---

## How KNN Works

### Step 1: Choose the Value of K

K represents the number of nearest neighbors considered for prediction.

Example:
- K = 3 → nearest 3 neighbors
- K = 5 → nearest 5 neighbors

---

### Step 2: Calculate Distance

The algorithm calculates the distance between the new point and all existing points.

Commonly used distance metric:
- Euclidean Distance

---

### Step 3: Find Nearest Neighbors

The nearest K data points are selected.

---

### Step 4: Make Prediction

- For Classification → majority voting  
- For Regression → average of neighbors  

---

## Euclidean Distance Formula

The distance between two points is calculated using:

d = √[(x₂ − x₁)² + (y₂ − y₁)²]

---

## Example

Suppose we want to classify a new fruit.

Nearby fruits:
- 4 Apples
- 1 Orange

Since most neighbors are Apples,
the new fruit will be classified as Apple.

---

## Choosing the Right Value of K

### Small K

- Sensitive to noise  
- May lead to overfitting  

### Large K

- Smoother predictions  
- May lead to underfitting  

Choosing the correct K is important for good performance.

---

## Visual Representation

![KNN](images/knn.png)

---

## Graph Explanation

- Nearby points influence prediction  
- The new point is classified based on nearest neighbors  
- Similar points form clusters naturally  

---

## Python Implementation

```python
import numpy as np
from sklearn.neighbors import KNeighborsClassifier

# Sample data
X = np.array([
    [1, 2],
    [2, 3],
    [3, 3],
    [6, 7],
    [7, 8],
    [8, 8]
])

# Labels
y = np.array([0, 0, 0, 1, 1, 1])

# Create model
model = KNeighborsClassifier(n_neighbors=3)

# Train model
model.fit(X, y)

# Predict
prediction = model.predict([[5, 5]])

print("Predicted Class:", prediction)
```

---

## KNN Visualization Graph Code

Run this code to generate the graph image:

```python
import matplotlib.pyplot as plt

# Class 0
x1 = [1, 2, 3]
y1 = [2, 3, 3]

# Class 1
x2 = [6, 7, 8]
y2 = [7, 8, 8]

# New point
new_x = [5]
new_y = [5]

plt.scatter(x1, y1, label="Class 0")
plt.scatter(x2, y2, label="Class 1")
plt.scatter(new_x, new_y, label="New Point")

plt.xlabel("X")
plt.ylabel("Y")
plt.title("KNN Visualization")
plt.legend()

plt.savefig("knn.png")
plt.show()
```

---

## Advantages

- Simple and easy to understand  
- No training phase required  
- Works well on small datasets  
- Effective for classification problems  

---

## Limitations

- Slow for large datasets  
- Sensitive to noise  
- Performance depends on K value  
- Requires feature scaling  

---

## Applications

- Recommendation Systems  
- Image Classification  
- Pattern Recognition  
- Medical Diagnosis  

---

## Key Takeaway

KNN is a simple yet powerful algorithm that predicts outcomes based on similarity between data points.

It is widely used for classification problems and helps build intuition about distance-based learning.

---



```md
![KNN](images/knn.png)
```
