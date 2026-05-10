# Supervised vs Unsupervised Learning

---

# Questions

1. [What is the difference between supervised, unsupervised, and reinforcement learning?](#q1)

2. [Difference between classification and regression?](#q2)

3. [How do decision trees work?](#q3)

4. [What is a random forest, and how does it work?](#q4)

5. [How does a random forest differ from a decision tree?](#q5)

6. [What is the difference between bagging and boosting?](#q6)

7. [What is cross-validation, and why is it important?](#q7)

---

# Answers

---

<a id="q1"></a>

# 1. What is the difference between supervised, unsupervised, and reinforcement learning?

| Supervised learning | Unsupervised Learning | Reinforcement learning |
|---|---|---|
| Model training with labeled data where each input has a corresponding/ known output. | Models are trained on unlabeled data. | A model learns by trial and error, receiving rewards or penalties based on its actions. |
| The model learns to predict the output for new, unseen inputs. | The goal is to find hidden patterns or structure in the data without explicit output labels. | It aims to make a sequence of decisions to maximize reward over time. |
| Decision Tree, Random Forest, Linear Regression, Logistic Regression | Examples: K-means clustering, Hierarchical clustering | Examples: Game-playing AI, Robot navigation, Self-driving cars |

---

<a id="q2"></a>

# 2. Difference between classification and regression?

| Classification | Regression |
|---|---|
| Where the output is a categorical variable | Where the output is a continuous variable |
| Ex: Spam vs non-spam, yes vs no. | Example: Predicting house prices, stock prices. |
| Defined labels | No labels defined |
| Algorithms: Naive Bayes, K-Nearest Neighbors (KNN), SVM, Logistic Regression | Algorithm: Linear regression, Polynomial regression, Ridge & Lasso regression. |

---

<a id="q3"></a>

# 3. How do decision trees work?

Answer:

A decision tree is a machine learning algorithm used for classification and regression tasks that makes decisions by splitting data into branches based on conditions or features.

- Root Node → First question
- Branch → Yes/No path
- Leaf Node → Final answer (crop name)
- Depth → How many questions deep

---

<a id="q4"></a>

# 4. What is a random forest, and how does it work?

Answer:

Random Forest is a machine learning algorithm that combines multiple decision trees to improve prediction accuracy and reduce overfitting. It works by training many decision trees on random subsets of data and combining their outputs.

---

<a id="q5"></a>

# 5. How does a random forest differ from a decision tree?

| Decision tree | Random forest |
|---|---|
| Overfitting easily | Resistant to overfitting |
| Accuracy is good. | Accuracy is lower on complex datasets |
| Accuracy is better. | Accuracy higher on complex datasets. |
| Training time is faster | Training time is slower |
| Handling high variance | Reduces variance |
| Works well on less datasets | Works well on large datasets |

---

<a id="q6"></a>

# 6. What is the difference between bagging and boosting?

Answer:

Bagging and boosting are ensemble learning techniques used to improve machine learning models.

Bagging trains multiple models independently and combines their results to reduce variance, while boosting trains models sequentially, where each new model focuses on correcting the errors of the previous model.

---

<a id="q7"></a>

# 7. What is cross-validation, and why is it important?

Answer:

Cross-validation is a technique for evaluating a model's performance on an individual dataset. It divides the dataset into subsets, usually the training, test, and validation sets.

This process is repeated multiple times to ensure the model generalizes well to unseen data and to stop overfitting.
