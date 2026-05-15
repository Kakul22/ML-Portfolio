# Support Vector Machine (SVM)

## Overview

Support Vector Machine (SVM) is a supervised Machine Learning algorithm used for both classification and regression tasks.

It is mainly used for classification problems and works by finding the best boundary that separates different classes.

---

## What is SVM?

SVM tries to find the optimal boundary between classes.

This boundary is called a:

### Hyperplane

👉 Simple idea:

"Find the best possible line or boundary that separates different categories."

---

## Hyperplane

A hyperplane is a decision boundary used to separate classes.

- In 2D → line  
- In 3D → plane  
- In higher dimensions → hyperplane  

---

## Support Vectors

Support Vectors are the nearest data points to the hyperplane.

These points are very important because they influence the position of the boundary.

---

## Margin

Margin is the distance between:
- support vectors
- and the hyperplane

### Goal of SVM

SVM tries to maximize the margin.

👉 Larger margin = better generalization

---

## How SVM Works

### Step 1: Plot Data Points

Data points are placed in feature space.

---

### Step 2: Find Hyperplane

The algorithm searches for the best separating boundary.

---

### Step 3: Maximize Margin

The boundary with the maximum margin is selected.

---

## Linear SVM

Used when data can be separated using a straight line.

Example:
- Pass / Fail
- Spam / Not Spam

---

## Non-Linear SVM

Sometimes data cannot be separated linearly.

In such cases, SVM uses:

### Kernel Trick

to transform data into higher dimensions.

---

## Types of Kernels

### Linear Kernel

Used for linearly separable data.

---

### Polynomial Kernel

Used for curved decision boundaries.

---

### RBF Kernel

Most commonly used kernel for complex datasets.

---

## Visual Representation

![SVM](images/svm.png)

---

## Graph Explanation

- Different classes are separated using a hyperplane  
- Support vectors are closest to the boundary  
- Maximum margin improves classification performance  

---

## Python Implementation

```python
from sklearn import svm

# Sample data
X = [
    [1, 2],
    [2, 3],
    [3, 3],
    [6, 7],
    [7, 8],
    [8, 8]
]

y = [0, 0, 0, 1, 1, 1]

# Model
model = svm.SVC(kernel='linear')

# Train
model.fit(X, y)

# Prediction
prediction = model.predict([[5, 5]])

print("Predicted Class:", prediction)
```

---

## Advantages

- Effective in high-dimensional data  
- Works well for classification tasks  
- Memory efficient  
- Powerful for complex datasets  

---

## Limitations

- Slow for very large datasets  
- Choosing the correct kernel is difficult  
- Harder to interpret  

---

## Applications

- Face Detection  
- Image Classification  
- Text Classification  
- Bioinformatics  

---

## Key Takeaway

SVM is a powerful classification algorithm that works by finding the optimal boundary between classes while maximizing the margin.

It performs well on both simple and complex datasets.

---


```md
![SVM](images/svm.png)
```
