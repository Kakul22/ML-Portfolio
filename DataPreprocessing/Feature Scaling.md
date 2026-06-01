# Feature Scaling

## Overview

Feature Scaling is a data preprocessing technique used to bring all features to a similar scale.

It prevents features with larger values from dominating features with smaller values.

---

## Why Do We Need Feature Scaling?

Consider the following features:

| Feature | Value |
|----------|----------|
| Age | 25 |
| Salary | 500000 |

Here Salary has much larger values than Age.

Algorithms that use distance calculations may give more importance to Salary and ignore Age.

Feature Scaling solves this problem.

---

## What is Feature Scaling?

Feature Scaling transforms data so that all features contribute equally to the model.

👉 Simple idea:

"Bring all features to a comparable range."

---

## When is Feature Scaling Required?

Feature Scaling is important for:

- KNN
- K-Means Clustering
- PCA
- Logistic Regression
- SVM
- Neural Networks

---

## When is Feature Scaling Not Necessary?

Usually not required for:

- Decision Trees
- Random Forests

because these algorithms do not rely on distance calculations.

---

## Types of Feature Scaling

### Standardization

Standardization transforms data so that:

- Mean = 0
- Standard Deviation = 1

Formula:

z = (x - μ) / σ

Where:

- x → original value
- μ → mean
- σ → standard deviation

---

### Example

Original Values:

```text
10, 20, 30, 40, 50
```

After Standardization:

```text
-1.41, -0.71, 0, 0.71, 1.41
```

---

## Normalization

Normalization scales values between 0 and 1.

Formula:

x' = (x - min) / (max - min)

---

### Example

Original Values:

```text
10, 20, 30, 40, 50
```

After Normalization:

```text
0, 0.25, 0.50, 0.75, 1.00
```

---

## Standardization vs Normalization

| Feature | Standardization | Normalization |
|----------|----------|----------|
| Range | No fixed range | 0 to 1 |
| Sensitive to Outliers | Less | More |
| Commonly Used For | ML Algorithms | Deep Learning |

---

## Visual Representation

![Feature Scaling](../images/feature_scaling.png)

---

## Graph Explanation

- Original data may have very different scales
- Scaling makes features comparable
- Distance-based algorithms perform better

---

## Python Implementation

### Standardization

```python
from sklearn.preprocessing import StandardScaler
import numpy as np

data = np.array([[10], [20], [30], [40], [50]])

scaler = StandardScaler()

scaled_data = scaler.fit_transform(data)

print(scaled_data)
```

---

### Normalization

```python
from sklearn.preprocessing import MinMaxScaler
import numpy as np

data = np.array([[10], [20], [30], [40], [50]])

scaler = MinMaxScaler()

scaled_data = scaler.fit_transform(data)

print(scaled_data)
```

---

## Advantages

- Improves model performance
- Faster convergence
- Better distance calculations
- Prevents feature dominance

---

## Limitations

- Additional preprocessing step
- Wrong scaling method may affect performance

---

## Applications

- KNN
- PCA
- K-Means Clustering
- Logistic Regression
- SVM
- Deep Learning

---

## Key Takeaway

Feature Scaling is one of the most important preprocessing techniques in Machine Learning.

It ensures that all features contribute equally and helps many algorithms perform better.

---

