# Train-Test Split

## Overview

In Machine Learning, we cannot evaluate a model using the same data on which it was trained.

To solve this, we divide the dataset into multiple parts:
- Training Set
- Validation Set
- Testing Set

This helps in building and evaluating a reliable model.

---

## Why Do We Need Data Splitting?

If we train and test on the same data:
- Model may memorize the data
- Performance will look artificially high

To avoid this, we use separate datasets.

---

## Types of Data Splits

### Training Set

- Used to train the model  
- Model learns patterns from this data  

---

### Validation Set

- Used to tune the model  
- Helps in selecting best parameters (hyperparameters)  

👉 Simple idea:
"Model ko improve karne ke liye use hota hai"

---

### Testing Set

- Used only for final evaluation  
- Should not be used during training  

👉 Yeh real-world performance batata hai

---

## Common Split Ratios

- 70% Training / 15% Validation / 15% Testing  
- 80% Training / 10% Validation / 10% Testing  

Depends on dataset size.

---

## Example

Suppose we have 100 data points:

- 70 → Training  
- 15 → Validation  
- 15 → Testing  

---

## Workflow

1. Train model using training data  
2. Tune model using validation data  
3. Evaluate final performance using test data  

---

## Python Example

```python
from sklearn.model_selection import train_test_split

X = [[1], [2], [3], [4], [5], [6], [7], [8]]
y = [2, 4, 6, 8, 10, 12, 14, 16]

# Step 1: Train + Temp
X_train, X_temp, y_train, y_temp = train_test_split(
    X, y, test_size=0.3, random_state=42
)

# Step 2: Validation + Test
X_val, X_test, y_val, y_test = train_test_split(
    X_temp, y_temp, test_size=0.5, random_state=42
)

print("Train:", X_train)
print("Validation:", X_val)
print("Test:", X_test)
