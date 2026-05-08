# Logistic Regression

## Overview

Logistic Regression is a supervised Machine Learning algorithm used for classification problems.

It predicts the probability that a data point belongs to a particular category.

---

## What is Logistic Regression?

Unlike Linear Regression, Logistic Regression is used when the output is categorical.

Examples:
- Spam or Not Spam  
- Disease or No Disease  
- Pass or Fail  

---

## Why Not Linear Regression for Classification?

Linear Regression predicts continuous values.

In classification problems, we need outputs between:
- 0 and 1  
- representing probabilities  

Logistic Regression solves this problem using the Sigmoid Function.

---

## Sigmoid Function

The sigmoid function converts values into probabilities between 0 and 1.

Formula:

σ(x) = 1 / (1 + e⁻ˣ)

---

## How Logistic Regression Works

1. Input data is provided  
2. Weighted sum is calculated  
3. Sigmoid function converts output into probability  
4. Probability is classified into categories  

Example:
- Probability > 0.5 → Positive Class  
- Probability < 0.5 → Negative Class  

---

## Graph Explanation

- Linear Regression gives a straight line  
- Logistic Regression gives an S-shaped curve  

This curve is called the Sigmoid Curve.

---

## Visual Representation

![Logistic Regression](images/logistic_regression.png)

---

## Python Implementation

```python
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LogisticRegression

# Sample data
X = np.array([[1], [2], [3], [4], [5], [6]])
y = np.array([0, 0, 0, 1, 1, 1])

# Model
model = LogisticRegression()
model.fit(X, y)

# Predictions
y_pred = model.predict(X)

print("Predictions:", y_pred)
