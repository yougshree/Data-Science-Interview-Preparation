# Pandas Interview Notes

---

# Questions

1. [What is Pandas?](#q1)

2. [What is a Series and DataFrame?](#q2)

3. [What does head() do?](#q3)

4. [How to Remove Null Values?](#q4)

5. [How to Remove Duplicates?](#q5)

6. [Difference Between List and Array?](#q6)

7. [How to Check Missing Values?](#q7)

8. [How to Explore a New Dataset?](#q8)

9. [What is groupby()?](#q9)

10. [How to Filter Data?](#q10)

11. [How to Select Columns?](#q11)

12. [Basic Aggregations?](#q12)

13. [Summary Table — All Functions](#q13)

14. [Exam Ready Answers](#q14)
---

# Answers

---

<a id="q1"></a>

## 1. What is Pandas?

```text
Definition:
Pandas is a Python library used for loading, exploring, cleaning and manipulating data in table format called DataFrame.
```

---

<a id="q2"></a>

## 2. What is a Series and DataFrame?

```text
Definition:
A Series is a one-dimensional labeled data structure.
A DataFrame is a 2D table with rows and columns —

Example:
N    P    K    Crop
90   42   43   Rice
85   58   41   Maize
60   55   44   Wheat

That table = DataFrame

```

---

<a id="q3"></a>

## 3. What does head() do?

```python
df.head()
# → Shows first 5 rows of data

df.head(10)
# → Shows first 10 rows
```

---

<a id="q4"></a>

## 4. How to Remove Null Values?

```python
# Two ways:

df.dropna()
# → Removes rows with
#   missing values completely

df.fillna(0)
# → Fills missing values with 0

df.fillna(df.mean())
# → Fills missing values
#   with column average

# When to use which?

# dropna() → Few missing values

# fillna() → Many missing values
#             don't want to lose rows
```

---

<a id="q5"></a>

## 5. How to Remove Duplicates?

```python
df.drop_duplicates()
# → Removes duplicate rows

df.duplicated().sum()
# → Count how many duplicates exist
```

---

<a id="q6"></a>

## 6. Difference Between List and Array?

```text
LIST (Python built-in)
→ Can hold mixed data types
→ [1, "hello", True, 3.14]
→ Slower for math operations
→ No math operations directly

ARRAY (NumPy)
→ Only one data type
→ [1, 2, 3, 4, 5]
→ Faster for math operations
→ Supports math directly
```

Example:

```python
list = [1, 2, 3]

list * 2
# [1,2,3,1,2,3]

array = np.array([1, 2, 3])

array * 2
# [2, 4, 6]
```

---

<a id="q7"></a>

## 7. How to Check Missing Values?

```python
df.isnull().sum()
# → Count missing values
#   per column
```

Output example:

```text
N              0
P              0
temperature    5
rainfall       2
```

---

<a id="q8"></a>

## 8. How to Explore a New Dataset?

```python
# Step by step — always do this:

df.head()        
# → see first 5 rows

df.shape         
# → rows and columns count

df.info()        
# → column names + data types

df.describe()    
# → mean, min, max, std

df.isnull().sum()
# → missing values

df.duplicated()  
# → duplicate rows

df.columns       
# → column names list
```

```text
This is called
Exploratory Data Analysis (EDA)
```

---

<a id="q9"></a>

## 9. What is groupby()?

```text
Definition:
groupby() groups rows by a
specific column and applies
aggregate functions
```

Example:

```python
df.groupby('district').mean()

# → Average loan amount
#   per district
```

---

<a id="q10"></a>

## 10. How to Filter Data?

```python
# Filter rows by condition:

df[df['temperature'] > 30]
# → Only farms where temp > 30

df[df['label'] == 'Rice']
# → Only Rice rows

# iFarmer example:

df[df['loan_status'] == 'Defaulted']
```

---

<a id="q11"></a>

## 11. How to Select Columns?

```python
# Single column:

df['crop']

# Multiple columns:

df[['N', 'P', 'K']]

# iFarmer example:

df[['farmer_name', 'loan_amount']]
```

---

<a id="q12"></a>

## 12. Basic Aggregations?

```python
df['rainfall'].mean()
# → average

df['rainfall'].max()
# → highest

df['rainfall'].min()
# → lowest

df['rainfall'].sum()
# → total

df['label'].value_counts()
# → count each category
```
```python
df['loan_amount'].mean()

# → Average loan given
```

---

<a id="q13"></a>

## 13. Summary Table — All Functions

| Function | What it Does |
|----------|-------------|
| pd.read_csv() | Load CSV file |
| df.head() | First 5 rows |
| df.tail() | Last 5 rows |
| df.shape | Rows and columns count |
| df.info() | Column names and types |
| df.describe() | Basic statistics |
| df.isnull().sum() | Count missing values |
| df.dropna() | Remove missing rows |
| df.fillna() | Fill missing values |
| df.duplicated() | Find duplicates |
| df.drop_duplicates() | Remove duplicates |
| df.groupby() | Group and aggregate |
| df.value_counts() | Count categories |

---

<a id="q14"></a>

### Q: What is Pandas?

> "Pandas is a Python library for data manipulation and analysis. It provides a DataFrame structure similar to a spreadsheet that allows loading, cleaning, filtering and analyzing structured data."

---
### Q: What is EDA?

> "EDA (Exploratory Data Analysis) is the process of analyzing and understanding a dataset using statistics and visualizations before building machine learning models."
---

### Q: How to read and save csv file?

> "read: pd.read_csv("data.csv")
>  save: df.to_csv("output.csv")"
---

### Q: Difference Between merge() and concat()?

> "merge() combines DataFrames using common columns,
> while concat() joins DataFrames vertically or horizontally."
---
### Q: What does head() do?

> "df.head() shows the first 5 rows of a DataFrame. It is the first thing a data scientist does when exploring a new dataset to quickly understand its structure."

---

### Q: How do you handle missing values?

> "First I check missing values using df.isnull().sum() to understand how many are missing. Missing values are handled using dropna() to remove rows with missing data or fillna() to replace them with a specific value like the mean." 
---

### Q: Difference between list and array?

> "A Python list can hold mixed data types but is slow for mathematical operations. A NumPy array holds only one data type but supports fast mathematical operations like multiplying all values at once."

---


