# Matplotlib

---

# Questions

1. [What is the difference between plt.show() and plt.savefig() in Matplotlib?](#q1)

2. [How can you create a histogram in Matplotlib?](#q2)

3. [How can you add a legend to a plot in Matplotlib?](#q3)

4. [What is the purpose of the plt.subplots() function in Matplotlib?](#q4)

5. [What is the difference between a scatter plot and a line plot in Matplotlib?](#q5)

6. [What is the difference between a bar plot and a histogram in Matplotlib?](#q6)

7. [How can you plot a line plot with multiple lines in Matplotlib?](#q7)

8. [How can you set the size of a plot in Matplotlib?](#q8)

9. [How can you create a scatter plot in Matplotlib?](#q9)

---

# Answers

---

<a id="q1"></a>

# 1. What is the difference between plt.show() and plt.savefig() in Matplotlib?

Answer:

plt.show()  
Used to display a chart as output.

plt.savefig()  
Used to save the chart as an image file.

---

<a id="q2"></a>

# 2. How can you create a histogram in Matplotlib?

Answer:

```python
import random

data = [random.randint(1, 10) for _ in range(100)]

#histogram continuous data
plt.hist(data, bins=10) #bins: how many parts in data

plt.title('Histogram')
plt.show()
```

---

<a id="q3"></a>

# 3. How can you add a legend to a plot in Matplotlib?

Answer:

```python
plt.legend()
```

A legend is a small box on a chart that explains what each line, bar or color represents.

Example:

```python
plt.plot(x,y1, label='Sales 2024')
plt.plot(x,y2, label= 'Sales 2025')

plt.title('year line char')
plt.xlabel('months')
plt.ylabel('sales')

plt.legend()
plt.show()
```

---

<a id="q4"></a>

# 4. What is the purpose of the plt.subplots() function in Matplotlib?

Answer:

```python
plt.subplot()
```

The plt.subplots() function is used to create multiple subplots in a single figure. It returns a tuple containing the figure object and an array of subplot objects.

Example:

```python
#subplot: used to show multiple charts in one figure

#1st plot: bar chart
plt.subplot(1,2,1) #row, col, pos

plt.bar(categories, sales)

plt.title('Daily sales Bar chart')
plt.xlabel('Week days')
plt.ylabel('Sales')


#2nd plot:scatter plot()
plt.subplot(1,2,2)

plt.scatter(categories, sales)

plt.title('Daily Sales Scatter plot')
plt.xlabel('Week days')
plt.ylabel('Sales')

plt.show()
```

---

<a id="q5"></a>

# 5. What is the difference between a scatter plot and a line plot in Matplotlib?

Answer:

Scatter Plot → Shows RELATIONSHIP between two variables  
No connection between points

Line Plot → Shows TREND over time or sequence  
Points ARE connected

---

<a id="q6"></a>

# 6. What is the difference between a bar plot and a histogram in Matplotlib?

Answer:

A bar plot displays discrete data as bars, while a histogram displays continuous data as bars that represent the frequency of data points in a given range.

| Type | Bar | Histogram |
|---|---|---|
| data | categorical | continious |
| x-axis | categorical | Number range |
| y-axis | count/value | frequency |
| variables | 2 variables | 1 variables |
| gaps | Gaps between bars | No gap |
| purpose | Compare group | Show distribution |

---

<a id="q7"></a>

# 7. How can you plot a line plot with multiple lines in Matplotlib?

Answer:

```python
x= [1,2,3,4,5]

y1= [10,20, 25, 35, 45]
y2= [20,30, 35, 45, 55]

plt.plot(x,y1, label='Sales 2024')
plt.plot(x,y2, label= 'Sales 2025')

plt.title('year line char')
plt.xlabel('months')
plt.ylabel('sales')

plt.legend()
plt.show()
```

---

<a id="q8"></a>

# 8. How can you set the size of a plot in Matplotlib?

Answer:

```python
plt.figure(figsize=(10,10))
```

---

<a id="q9"></a>

# 9. How can you create a scatter plot in Matplotlib?

Answer:

```python
y1= [10,20, 25, 35, 45]
y2= [20,30, 35, 45, 55]

#Scatter plot: relation between variables
plt.scatter(y1, y2)

plt.title('Scatter Plot')
plt.show()
```
