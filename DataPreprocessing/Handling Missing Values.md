# Handling Missing Values

## Overview

Missing values are one of the most common problems in real-world datasets.

They occur when some information is unavailable, incomplete, or not recorded.

Before training a Machine Learning model, missing values must be handled properly.

---

## What are Missing Values?

Missing values are data points that contain no value.

They are usually represented as:

- NaN (Not a Number)
- NULL
- Empty Cells

Example:

| Name | Age | Salary |
|--------|--------|--------|
| John | 25 | 50000 |
| Alice | NaN | 60000 |
| Bob | 30 | NaN |

---

## Why Missing Values are a Problem?

Missing values can:

- Reduce model accuracy
- Cause training errors
- Create biased predictions
- Affect statistical analysis

Therefore, handling missing values is an important preprocessing step.

---

## Types of Missing Data

### Missing Completely At Random (MCAR)

Missing values have no relationship with any feature.

Example:
- Survey form accidentally lost.

---

### Missing At Random (MAR)

Missing values depend on another feature.

Example:
- Salary missing for some age groups.

---

### Missing Not At Random (MNAR)

Missing values depend on the missing value itself.

Example:
- People with very high salaries choose not to disclose salary.

---

## Methods to Handle Missing Values

### 1. Remove Missing Values

Rows or columns containing missing values are deleted.

Suitable when:
- Only a small portion of data is missing.

---

### Example

Before:

| Age | Salary |
|------|------|
| 25 | 50000 |
| NaN | 60000 |

After removing:

| Age | Salary |
|------|------|
| 25 | 50000 |

---

## 2. Mean Imputation

Replace missing values with the mean.

Example:

Ages:

20, 25, NaN, 35

Mean:

(20 + 25 + 35) / 3 = 26.67

Result:

20, 25, 26.67, 35

---

## 3. Median Imputation

Replace missing values with the median.

Useful when outliers are present.

---

### Example

Data:

10, 20, NaN, 30, 1000

Median:

20

Result:

10, 20, 20, 30, 1000

---

## 4. Mode Imputation

Replace missing values with the most frequent value.

Used for categorical data.

---

### Example

Colors:

Red, Blue, Red, NaN

Mode:

Red

Result:

Red, Blue, Red, Red

---

## 5. Forward Fill

Replace missing values using previous values.

Example:

| Day | Sales |
|------|------|
| 1 | 100 |
| 2 | NaN |
| 3 | 120 |

Result:

| Day | Sales |
|------|------|
| 1 | 100 |
| 2 | 100 |
| 3 | 120 |

---

## 6. Backward Fill

Replace missing values using next available value.

---

## Visual Representation

![Missing Values](../images/missing_values.png)

---

## Graph Explanation

- Missing values create gaps in data
- Imputation techniques fill these gaps
- Better quality data improves model performance

---

## Python Implementation

### Detect Missing Values

```python
import pandas as pd

df = pd.read_csv("data.csv")

print(df.isnull().sum())
```

---

### Mean Imputation

```python
df["Age"].fillna(df["Age"].mean(), inplace=True)
```

---

### Median Imputation

```python
df["Age"].fillna(df["Age"].median(), inplace=True)
```

---

### Mode Imputation

```python
df["City"].fillna(df["City"].mode()[0], inplace=True)
```

---

## Advantages

- Improves data quality
- Prevents training errors
- Helps maintain dataset size

---

## Limitations

- Incorrect imputation may introduce bias
- Too many missing values can reduce reliability

---

## Applications

- Healthcare Data
- Financial Data
- Customer Analytics
- Survey Analysis

---

## Key Takeaway

Handling Missing Values is a critical preprocessing step in Machine Learning.

Proper treatment of missing data helps improve model accuracy, reliability, and overall performance.

---
