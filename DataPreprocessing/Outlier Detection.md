# Outlier Detection

## Overview

Outlier Detection is the process of identifying data points that significantly differ from the rest of the dataset.

These unusual observations are called Outliers.

Outliers can negatively impact Machine Learning models and statistical analysis.

---

## What is an Outlier?

An Outlier is a data point that is very different from other observations.

Example:

```text
10, 12, 15, 18, 20, 500
```

Here:

```text
500
```

is an outlier because it is far away from the other values.

---

## Why Are Outliers Important?

Outliers can:

- Reduce model accuracy
- Distort statistical measures
- Affect feature scaling
- Lead to incorrect predictions

Therefore, detecting and handling outliers is an important preprocessing step.

---

## Types of Outliers

### Global Outlier

A value that is extremely different from the entire dataset.

Example:

```text
5, 7, 8, 10, 1000
```

---

### Contextual Outlier

A value that is unusual in a specific context.

Example:

Temperature:

```text
35°C in Summer → Normal
35°C in Winter → Outlier
```

---

### Collective Outlier

A group of observations that together behave abnormally.

Example:

A sudden spike in network traffic indicating a cyberattack.

---

## Methods to Detect Outliers

### 1. Z-Score Method

Measures how far a data point is from the mean.

Formula:

```
Z = (X - Mean) / Standard Deviation
```

Generally:

```text
|Z| > 3
```

indicates an outlier.

---

## Visual Representation


::contentReference[oaicite:0]{index=0}


---

### Example

Data:

```text
10, 12, 15, 18, 20, 100
```

The value:

```text
100
```

will have a very high Z-score and may be considered an outlier.

---

## 2. IQR Method (Interquartile Range)

One of the most commonly used techniques.

### Step 1

Find:

- Q1 (25th percentile)
- Q3 (75th percentile)

---

### Step 2

Calculate:

```
IQR = Q3 - Q1
```

---

### Step 3

Calculate bounds:

```
Lower Bound = Q1 - 1.5 × IQR

Upper Bound = Q3 + 1.5 × IQR
```

Values outside these bounds are considered outliers.

---

## Visual Representation

![IQR Outlier Detection](../images/iqr_outlier.png)

---

## 3. Box Plot

A Box Plot visually identifies outliers.

Points outside the whiskers are considered outliers.

---

## Visual Representation

![Box Plot](../images/boxplot_outlier.png)

---

## 4. Isolation Forest

Isolation Forest is a Machine Learning algorithm specifically designed for anomaly detection.

It isolates unusual observations using random trees.

---

## 5. DBSCAN

DBSCAN can identify sparse points as noise.

These noise points are often treated as outliers.

---

## Handling Outliers

### Remove Outliers

Used when outliers are clearly incorrect.

---

### Replace Outliers

Replace using:

- Mean
- Median
- Mode

---

### Cap Outliers

Limit extreme values to a threshold.

This technique is called:

### Winsorization

---

## Python Implementation

### Z-Score Method

```python
from scipy import stats
import numpy as np

data = np.array([10,12,15,18,20,100])

z_scores = np.abs(stats.zscore(data))

print(z_scores)
```

---

### IQR Method

```python
import pandas as pd

data = pd.Series([10,12,15,18,20,100])

Q1 = data.quantile(0.25)
Q3 = data.quantile(0.75)

IQR = Q3 - Q1

lower = Q1 - 1.5 * IQR
upper = Q3 + 1.5 * IQR

outliers = data[(data < lower) | (data > upper)]

print(outliers)
```

---

## Advantages

- Improves model performance
- Reduces noise
- Produces more reliable predictions

---

## Limitations

- Genuine rare events may be removed
- Detection method depends on data distribution

---

## Applications

- Fraud Detection
- Intrusion Detection
- Healthcare Analytics
- Financial Analysis
- Quality Control

---

## Key Takeaway

Outlier Detection helps identify unusual observations that may negatively affect Machine Learning models.

Proper handling of outliers improves data quality, model performance, and prediction reliability.

---

