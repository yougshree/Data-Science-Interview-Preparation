# Hypothesis Testing

Read link: https://www.datacamp.com/tutorial/hypothesis-testing  
Read link: https://www.datacamp.com/blog/data-scientist-interview-questions  

---

# Questions

1. [What is hypothesis testing?](#q1)

2. [What is a P-Value?](#q2)

3. [What is the null hypothesis, and how do you determine whether to reject it?](#q3)

4. [What Tests Are Used to Get the P-Value?](#q4)

5. [When would you use a t-test vs. a z-test?](#q5)

6. [What is the difference between a Type I and a Type II error?](#q6)

7. [What Is A/B Testing?](#q7)

8. [How do you handle a dataset missing several values?](#q8)

9. [How can you avoid overfitting your model?](#q9)

10. [How can you avoid underfitting your model?](#q10)

---

# Answers

---

<a id="q1"></a>

# 1. What is hypothesis testing?

Answer: Hypothesis testing is a statistical method used to make decisions about a population based on sample data. It tests whether an assumption is true or false.

Example: iFarmer assumes that farmers who use fertilizer produce more crops. Hypothesis testing checks if this is actually true using real data.

Null Hypothesis (H0): This is the default assumption that there is no effect or difference.  

Alternative Hypothesis (Ha): This is the hypothesis that there is an effect or difference.

---

<a id="q2"></a>

# 2. What is a P-Value?

Answer: A p-value measures the probability of observing results at least as extreme as the data collected, assuming the null hypothesis is true.

![P-Value](images/p_value.png)

P-value < 0.05 → Result is significant → Reject H0  

P-value > 0.05 → Result is by chance → Accept H0

---

<a id="q3"></a>

# 3. What is the null hypothesis, and how do you determine whether to reject it?

The null hypothesis is the default assumption that there is NO relationship or effect between variables.

Example:

H0 = "Soil nutrients have NO effect on crop yield"  

H1 = "Soil nutrients DO affect crop yield"

Reject:

If P-value < 0.05 → Reject H0 → Your finding is significant  

If P-value > 0.05 → Fail to reject H0 → No significant finding.

---

<a id="q4"></a>

# 4. What Tests Are Used to Get the P-Value?

Answer:

| Test | When to Use |
|---|---|
| T-test | Compare the means of 2 groups |
| Z-test | Large sample size (n>30) |
| Chi-square test | Categorical data |

---

<a id="q5"></a>

# 5. When would you use a t-test vs. a z-test?

Answer:

| T-test | Z-test |
|---|---|
| Sample Size | Small (n < 30) |
| Population standard deviation | Unknown |
| Example | 20 farmers sample |

| Z-test |  |
|---|---|
| Sample Size | Large (n > 30) |
| Population standard deviation | Known |
| Example | 500 farmers sample |

---

<a id="q6"></a>

# 6. What is the difference between a Type I and a Type II error?

Answer:

Type I error (false positive): Rejecting the null hypothesis when it is actually true. The alarm goes off for nothing. Controlled by your significance level (α). Example: concluding a new model performs better when it actually doesn't.

Type II error (false negative): Failing to reject the null hypothesis when it is false. Missed a real problem. Controlled by statistical power (1 − β). Example: Concluding a model shows no improvement when it actually does.

---

<a id="q7"></a>

# 7. What Is A/B Testing?

Answer:

"A/B Testing is a controlled experiment that compares two versions of something to determine which performs better. Version A is the control, and Version B is the variation. The audience is randomly split between both versions and results are measured using statistical hypothesis testing. For example, iFarmer could use A/B testing to compare two different loan application page designs and see which one gets more farmer sign-ups."

---

<a id="q8"></a>

# 8. How do you handle a dataset missing several values?

Answer:

- Drop the rows with missing values.
- Drop the columns with several missing values.
- Fill the missing value with a string or numerical constant.
- Replace the missing values with the average or median value of the column.
- Use multiple-regression analyses to estimate a missing value.
- Use multiple columns to replace missing values with average simulated values and random errors.

---

<a id="q9"></a>

# 9. How can you avoid overfitting your model?

Answer:

Overfitting refers to a model that is trained too well on a training dataset but fails on the test and validation datasets.

- Keeping the model simple by decreasing the model complexity, taking fewer variables into account, and reducing the number of parameters in neural networks.
- Using cross-validation techniques.
- Training the model with more data.
- Using data augmentation that increases the number of samples.
- Using ensembling (Bagging and Boosting)
- Using regularization techniques to penalize certain model parameters if they're likely to cause overfitting.
<a id="q10"></a>

# 9. How can you avoid underfitting your model?

Answer: 
When the model is too simple, it cannot learn patterns and gives bad accuracy on both training and test data.
Increase model complexity.
Add more features.
Training longer/ more iterations.
Use a better algorithm
 
