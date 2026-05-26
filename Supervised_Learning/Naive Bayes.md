# Naive Bayes

## Overview

Naive Bayes is a supervised Machine Learning algorithm mainly used for classification problems.

It is based on Bayes' Theorem and assumes that all features are independent of each other.

---

## What is Naive Bayes?

Naive Bayes predicts the probability of a data point belonging to a particular class.

👉 Simple idea:

"Calculate probabilities and choose the class with the highest probability."

---

## Why is it Called "Naive"?

The algorithm assumes that:
- all features are independent
- one feature does not affect another

This assumption is called "naive".

Example:
In reality:
- age
- salary
- experience

may be related.

But Naive Bayes assumes they are independent.

---

## Bayes' Theorem

Naive Bayes works using Bayes' Theorem.

Formula:

P(A|B) = [P(B|A) × P(A)] / P(B)

Where:
- P(A|B) → probability of A given B
- P(B|A) → probability of B given A
- P(A) → probability of A
- P(B) → probability of B

---

## How Naive Bayes Works

### Step 1: Calculate Prior Probability

Probability of each class.

---

### Step 2: Calculate Likelihood

Probability of features for each class.

---

### Step 3: Apply Bayes' Theorem

Combine probabilities.

---

### Step 4: Predict Final Class

Choose the class with highest probability.

---

## Types of Naive Bayes

### Gaussian Naive Bayes

Used for continuous numerical data.

---

### Multinomial Naive Bayes

Used for text classification.

---

### Bernoulli Naive Bayes

Used for binary features.

---

## Visual Representation

![Naive Bayes](../images/naive_bayes.png)

---

## Graph Explanation

- Features contribute independently to prediction  
- Probabilities are calculated for each class  
- Final class is selected using maximum probability  

---

## Python Implementation

```python
from sklearn.naive_bayes import GaussianNB

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
model = GaussianNB()

# Train
model.fit(X, y)

# Prediction
prediction = model.predict([[5, 6]])

print("Predicted Class:", prediction)
```

---

## Advantages

- Fast and efficient  
- Works well on large datasets  
- Performs well in text classification  
- Requires less training data  

---

## Limitations

- Assumes feature independence  
- May perform poorly if assumptions are incorrect  
- Zero probability problem may occur  

---

## Applications

- Spam Detection  
- Sentiment Analysis  
- Recommendation Systems  
- Document Classification  

---

## Key Takeaway

Naive Bayes is a simple yet powerful probabilistic algorithm widely used for classification tasks, especially in Natural Language Processing (NLP).

---

