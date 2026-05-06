# Linear Regression

## Overview

Linear Regression is one of the simplest and most fundamental algorithms in Machine Learning.

It is used to model the relationship between a dependent variable (target) and one or more independent variables (features).

---

## What is Linear Regression?

Linear Regression tries to find a straight line that best fits the data points.

👉 Simple idea:
"Find a line that represents the trend in the data"

---

## Equation of Linear Regression

The mathematical equation is:

y = mx + b

Where:
- y → dependent variable (output)
- x → independent variable (input)
- m → slope of the line
- b → intercept (value of y when x = 0)

---

## How It Works

The model finds the best values of m and b such that the error between predicted values and actual values is minimized.

👉 It uses optimization techniques like minimizing the Mean Squared Error (MSE).

---

## Graph Explanation

- Data points are plotted on a graph  
- A straight line is drawn through them  
- This line is called the "Best Fit Line"  

The goal is to minimize the distance between actual points and the line.

---

## Visual Representation

![Linear Regression](images/linear_regression.png)

---

## Python Implementation

```python
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

# Sample data
X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
y = np.array([2, 4, 6, 8, 10])

# Model
model = LinearRegression()
model.fit(X, y)

# Predictions
y_pred = model.predict(X)

# Plot
plt.scatter(X, y)
plt.plot(X, y_pred)

plt.xlabel("X")
plt.ylabel("y")
plt.title("Linear Regression")

plt.savefig("linear_regression.png")
plt.show()
