# Types of Machine Learning
 Overview

** Machine Learning can be broadly categorized into three main types based on how the model learns from data:**

Supervised Learning  
Unsupervised Learning  
Reinforcement Learning

Each type has a different learning approach and is used for different kinds of problems.

## 1. Supervised Learning

Supervised Learning is a type of Machine Learning where the model is trained on labeled data.
This means:

Input data (features X) and output (target y) are already known
The model learns a mapping from input to output
Simple Idea:
**"Model ko sahi answers pe train karte hain, taaki vo future me correct prediction kar sake."**

📌 Example
Study Hours	Marks  
2	40  
4	60

The model learns:

More study hours → higher marks

## Types of Supervised Learning 

**Regression**  
Output is continuous  
Example: predicting house price 🏠

**Classification**  
Output is categorical  
Example: spam vs not spam 📧

**Common Algorithms**  
Linear Regression  
Logistic Regression  
K-Nearest Neighbors (KNN)  
Decision Trees  
Random Forest

## 2. Unsupervised Learning
Unsupervised Learning deals with unlabeled data.

This means:

Only input data is given  
No correct output is provided  
The model tries to discover hidden patterns on its own
Simple Idea:

**"Yahan model ko answer nahi diya jata — vo khud data me structure dhundta hai."**

📌 Example
Customer segmentation in a shopping dataset:  
The model automatically groups customers into categories like:

High spenders  
Medium spenders  
Low spenders
## Types of Unsupervised Learning  

**Clustering**  
Grouping similar data points  
Association  
Finding relationships between variables
**Common Algorithms** 

K-Means Clustering  
Hierarchical Clustering  
Principal Component Analysis (PCA)

## 3. Reinforcement Learning

Reinforcement Learning is based on learning through interaction with an environment.

It involves:  
Agent (learner)  
Environment (where agent acts)  
Reward/Penalty system
Simple Idea:

**"Sahi action → reward, galat action → penalty → model gradually improve karta hai."**

📌 Example
Game-playing AI 🎮  
Correct move → reward  
Wrong move → penalty

Over time, the agent learns the best strategy.

**Applications**  
Self-driving cars 🚗  
Robotics 🤖
Game AI (like chess, AlphaGo)
**Comparison Table**  
Feature	                  Supervised               Learning	Unsupervised       Learning	Reinforcement Learning  
Data	                    Labeled	                 Unlabeled	                 Environment-based  
Goal	                    Predict output           Find hidden patterns	       Maximize reward  
HumanGuidance	            High	                   Low	                       Medium

Example	Spam detection	Customer segmentation	Game AI

 **When to Use What?**
Use Supervised Learning → when you have labeled data  
Use Unsupervised Learning → when you want to explore patterns  
Use Reinforcement Learning → when decisions depend on actions over time

✨ Final Note

Understanding these three types is essential because almost every Machine Learning problem falls into one of these categories.
