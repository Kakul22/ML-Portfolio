# Decision Tree

## Overview

Decision Tree is a supervised Machine Learning algorithm used for both classification and regression problems.

It works like a flowchart where:
- each internal node represents a condition
- each branch represents a decision
- each leaf node represents the final output

---

## What is a Decision Tree?

A Decision Tree splits the dataset into smaller parts based on conditions.

👉 Simple idea:

"Ask questions step-by-step until a final decision is reached."

---

## Real-Life Example

Suppose we want to decide whether to play cricket or not.

Questions can be:
- Is the weather sunny?
- Is it raining?
- Is humidity high?

Based on answers, the final decision is made.

---

## Structure of a Decision Tree

### Root Node

- Starting point of the tree  
- Represents the entire dataset  

---

### Internal Node

- Represents conditions or decisions  
- Example: Age > 18  

---

### Branch

- Represents outcomes of conditions  

---

### Leaf Node

- Final output or prediction  

---

## How Decision Tree Works

### Step 1: Select Best Feature

The algorithm chooses the best feature to split the data.

---

### Step 2: Split the Dataset

Data is divided into smaller subsets.

---

### Step 3: Repeat Recursively

The process continues until:
- pure nodes are obtained
- stopping condition is reached

---

## Entropy

Entropy measures the impurity or randomness in the dataset.

### Formula

Entropy = -p log₂(p) - q log₂(q)

Where:
- p → probability of class 1
- q → probability of class 2

---

## Information Gain

Information Gain measures how much uncertainty is reduced after splitting.

👉 Higher Information Gain = Better Feature

---

## Visual Representation

![Decision Tree](images/decision_tree.png)

---

## Graph Explanation

- The root node starts the decision process  
- Branches represent conditions  
- Leaf nodes represent final predictions  

---

## Python Implementation

```python
from sklearn.tree import DecisionTreeClassifier
from sklearn import tree
import matplotlib.pyplot as plt

# Sample data
X = [[1], [2], [3], [4], [5], [6]]
y = [0, 0, 0, 1, 1, 1]

# Model
model = DecisionTreeClassifier()

# Train
model.fit(X, y)

# Plot tree
plt.figure(figsize=(8,6))
tree.plot_tree(model, filled=True)

plt.savefig("decision_tree.png")
plt.show()
```

---

## Advantages

- Easy to understand and visualize  
- Handles both numerical and categorical data  
- Requires less data preprocessing  

---

## Limitations

- Can easily overfit  
- Sensitive to small data changes  
- Large trees become complex  

---

## Applications

- Medical Diagnosis  
- Fraud Detection  
- Customer Segmentation  
- Risk Analysis  

---

## Key Takeaway

Decision Trees are powerful and intuitive algorithms that make decisions using a tree-like structure.

They are widely used because they are easy to understand and interpret.

---



```md
![Decision Tree](images/decision_tree.png)
```
