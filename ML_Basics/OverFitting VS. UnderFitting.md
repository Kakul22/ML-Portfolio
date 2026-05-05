# Overfitting vs Underfitting
Overview

In Machine Learning, one of the most important challenges is ensuring that a model performs well not only on training data but also on unseen data.

Two common problems that occur during model training are:

**Overfitting**  
**Underfitting**

## Underfitting  
Underfitting occurs when a model is too simple to capture the underlying patterns in the data.

Key Idea
The model fails to learn the relationship between input and output properly.

### Characteristics  
Poor performance on training data  
Poor performance on testing data  
Model is too simple

Example  
Suppose you are trying to fit a straight line to data that actually follows a curve.

The model cannot capture the complexity → results in wrong predictions.

### Causes  
Model too simple  
Not enough training  
Insufficient features  
How to Fix Underfitting  
Use a more complex model  
Increase training time  
Add more relevant features

## Overfitting
Overfitting occurs when a model learns the training data too well, including noise and unnecessary details.

Key Idea

The model memorizes the data instead of learning general patterns.

### Characteristics  
Very high accuracy on training data  
Poor performance on testing data  
Model is too complex

Example
A model that perfectly remembers all training examples but fails on new data.

### Causes  
Model too complex  
Too many features  
Small dataset  
How to Fix Overfitting  
Use more training data  
Apply regularization  
Reduce model complexity  
Use techniques like dropout (in deep learning)  
Visual Intuition

Underfitting → model is too simple (high error everywhere)
Good fit → model captures pattern correctly
Overfitting → model is too complex (fits even noise)

Comparison  
Aspect	                   Underfitting	           Overfitting  
ModelComplexity	            Low	                   High  
Training Accuracy	          Low                    Very High  
Testing Accuracy	          Low	                   Low  
Generalization	            Poor	                 Poor  

**Why It Matters**

The goal of Machine Learning is not just to perform well on training data but to generalize well on new, unseen data.

A good model should maintain a balance between underfitting and overfitting.

Key Takeaway

A perfect model is one that:  
Learns patterns from training data  
Does not memorize noise  
Performs well on unseen data
