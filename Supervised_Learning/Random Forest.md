# Random Forest

## Overview

Random Forest is a supervised Machine Learning algorithm used for both classification and regression tasks.

It is an ensemble learning method that combines multiple Decision Trees to improve accuracy and reduce overfitting.

---

## What is Random Forest?

Random Forest creates many Decision Trees and combines their predictions to produce a final result.

👉 Simple idea:

"Instead of relying on one tree, use multiple trees and take the majority decision."

---

## Why Random Forest is Better than a Single Decision Tree

A single Decision Tree:
- may overfit
- may be sensitive to data changes

Random Forest solves this problem by:
- creating multiple trees
- training them on different subsets of data
- combining their outputs

This improves stability and accuracy.

---

## How Random Forest Works

### Step 1: Create Multiple Random Samples

Different subsets of the dataset are created using random sampling.

---

### Step 2: Build Decision Trees

A separate Decision Tree is trained on each subset.

---

### Step 3: Make Predictions

Each tree gives its own prediction.

---

### Step 4: Final Output

- For Classification → Majority Voting  
- For Regression → Average Prediction  

---

## Ensemble Learning

Random Forest is an example of Ensemble Learning.

Ensemble Learning means:
- combining multiple models
- to achieve better performance

---

## Bagging Technique

Random Forest uses a technique called:

### Bootstrap Aggregation (Bagging)

It:
- creates random subsets of data
- trains different trees
- combines results

This reduces variance and improves performance.

---

## Visual Representation

![Random Forest](images/random_forest.png)

---

## Graph Explanation

- Multiple Decision Trees are created  
- Each tree makes predictions independently  
- Final prediction is obtained by combining outputs  

---

## Python Implementation

```python
from sklearn.ensemble import RandomForestClassifier

# Sample data
X = [
    [1, 2],
    [2, 3],
    [3, 4],
    [6, 7],
    [7, 8],
    [8, 9]
]

y = [0, 0, 0, 1, 1, 1]

# Model
model = RandomForestClassifier(n_estimators=5)

# Train model
model.fit(X, y)

# Prediction
prediction = model.predict([[5, 6]])

print("Predicted Class:", prediction)
```

---

## Advantages

- High accuracy  
- Reduces overfitting  
- Works well on large datasets  
- Handles missing values effectively  

---

## Limitations

- Slower than Decision Trees  
- More computationally expensive  
- Harder to interpret  

---

## Applications

- Fraud Detection  
- Recommendation Systems  
- Medical Diagnosis  
- Stock Market Prediction  

---

## Key Takeaway

Random Forest combines the power of multiple Decision Trees to create a more accurate and reliable Machine Learning model.

It is one of the most widely used algorithms in real-world Machine Learning applications.

---

## Folder Structure

```text
Supervised_Learning/
│
├── Random_Forest.md
├── images/
│   └── random_forest.png
```

---

## Markdown Image Code

```md
![Random Forest](images/random_forest.png)
```
