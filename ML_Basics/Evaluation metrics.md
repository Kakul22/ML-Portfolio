# Evaluation Metrics

## Overview

After training a Machine Learning model, it is important to evaluate how well it performs on unseen data.

Evaluation metrics help us measure the effectiveness of a model.

Different types of problems use different metrics:
- Classification → Accuracy, Precision, Recall, F1 Score  
- Regression → MAE, MSE, RMSE  

---

## Confusion Matrix

A Confusion Matrix is a table used to evaluate the performance of a classification model.

It compares actual values with predicted values.

|                | Predicted Positive | Predicted Negative |
|----------------|-------------------|-------------------|
| Actual Positive | True Positive (TP) | False Negative (FN) |
| Actual Negative | False Positive (FP) | True Negative (TN) |

---

## Understanding TP, TN, FP, FN

### True Positive (TP)

The model correctly predicts a positive case.

Example:
- Actual: Spam  
- Predicted: Spam  

---

### True Negative (TN)

The model correctly predicts a negative case.

Example:
- Actual: Not Spam  
- Predicted: Not Spam  

---

### False Positive (FP)

The model incorrectly predicts a positive case.

Example:
- Actual: Not Spam  
- Predicted: Spam  

This is also called a False Alarm (Type I Error).

---

### False Negative (FN)

The model incorrectly predicts a negative case.

Example:
- Actual: Spam  
- Predicted: Not Spam  

This is also called a Missed Case (Type II Error).

---

## Real-Life Example

Consider a disease detection system:

- TP → Sick person correctly identified as sick  
- TN → Healthy person correctly identified as healthy  
- FP → Healthy person wrongly identified as sick  
- FN → Sick person wrongly identified as healthy  

---

## Accuracy

Accuracy measures the proportion of correct predictions.

Accuracy = (TP + TN) / (TP + TN + FP + FN)

### When to Use

- When dataset is balanced  
- When all types of errors are equally important  

---

## Precision

Precision measures how many predicted positive cases are actually correct.

Precision = TP / (TP + FP)

### When to Use

- When false positives are costly  
- Example: Spam detection  

---

## Recall

Recall measures how many actual positive cases are correctly predicted.

Recall = TP / (TP + FN)

### When to Use

- When missing positive cases is dangerous  
- Example: Disease detection  

---

## F1 Score

F1 Score is the harmonic mean of Precision and Recall.

F1 Score = 2 × (Precision × Recall) / (Precision + Recall)

### When to Use

- When you need a balance between Precision and Recall  

---

## Regression Metrics

### Mean Absolute Error (MAE)

Measures the average absolute difference between actual and predicted values.

MAE = (1/n) × Σ |Actual − Predicted|

---

### Mean Squared Error (MSE)

Measures the average of squared differences.

MSE = (1/n) × Σ (Actual − Predicted)²

---

### Root Mean Squared Error (RMSE)

Square root of Mean Squared Error.

RMSE = √MSE

---

## Comparison

| Metric | Use Case |
|--------|---------|
| Accuracy | Balanced datasets |
| Precision | When false positives matter |
| Recall | When false negatives matter |
| F1 Score | Balance between precision and recall |
| MAE | Simple error measurement |
| MSE | Penalizes large errors |
| RMSE | Same unit as output |

---

## Key Takeaway

Choosing the right evaluation metric is important because it directly affects how we judge model performance.

A model with high accuracy is not always the best model. The choice of metric depends on the problem.
