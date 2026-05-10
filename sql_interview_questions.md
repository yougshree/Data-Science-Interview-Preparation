# Questions

1. [Select all rows from a table](#q1)

2. [Filter rows using WHERE](#q2)

3. [Sort data (ORDER BY)](#q3)

4. [Limit results (TOP / LIMIT)](#q4)

5. [Count total rows](#q5)

6. [Average salary](#q6)

7. [Sum of column](#q7)

8. [Group by department](#q8)

9. [Count per group](#q9)

10. [Having clause (filter groups)](#q10)

11. [Find NULL values](#q11)

12. [Remove duplicates](#q12)

13. [Second highest salary ](#q13)

14. [Top 5 highest salaries](#q14)

15. [Join two tables (INNER JOIN)](#q15)

16. [Left join concept](#q16)

17. [Find max salary](#q17)

18. [Find min salary](#q18)

19. [Employees with salary between range](#q19)

20. [Find duplicates in a column](#q20)

21. [Write a solution to find the employees who earn more than their managers.](#q21)
   
22. [ Write a solution to delete all duplicate emails, keeping only one unique email with the smallest id.](#q22)

---

# Answers

---

<a id="q1"></a>

## 1. Select all rows from a table

```sql
SELECT * FROM employees;
```

---

<a id="q2"></a>

## 2. Filter rows using WHERE

```sql
SELECT * FROM employees
WHERE salary > 50000;
```

---

<a id="q3"></a>

## 3. Sort data (ORDER BY)

```sql
SELECT * FROM employees
ORDER BY salary DESC;
```

---

<a id="q4"></a>

## 4. Limit results (TOP / LIMIT)

```sql
SELECT * FROM employees
LIMIT 5;
```

---

<a id="q5"></a>

## 5. Count total rows

```sql
SELECT COUNT(*) FROM employees;
```

---

<a id="q6"></a>

## 6. Average salary

```sql
SELECT AVG(salary) FROM employees;
```

---

<a id="q7"></a>

## 7. Sum of column

```sql
SELECT SUM(salary) FROM employees;
```

---

<a id="q8"></a>

## 8. Group by department

```sql
SELECT department, AVG(salary)
FROM employees
GROUP BY department;
```

---

<a id="q9"></a>

## 9. Count per group

```sql
SELECT department, COUNT(*)
FROM employees
GROUP BY department;
```

---

<a id="q10"></a>

## 10. Having clause (filter groups)

```sql
SELECT department, COUNT(*)
FROM employees
GROUP BY department
HAVING COUNT(*) > 5;
```

---

<a id="q11"></a>

## 11. Find NULL values

```sql
SELECT * FROM employees
WHERE salary IS NULL;
```

---

<a id="q12"></a>

## 12. Remove duplicates 

```sql
SELECT DISTINCT department FROM employees;
```

---

<a id="q13"></a>

## 13. Write a solution to find the second highest distinct salary from the Employee table. If there is no second highest salary, return null

```sql
select max(salary) as  SecondHighestSalary
from Employee
where salary<(select max(salary) 
              from Employee);
#MAX() returns NULL if there is no 2nd higest salary
```

---

<a id="q14"></a>

## 14. Top 5 highest salaries

```sql
SELECT * FROM employees
ORDER BY salary DESC
LIMIT 5;
```

---

<a id="q15"></a>

## 15. Join two tables (INNER JOIN)

```sql
SELECT e.name, d.department_name
FROM employees e
INNER JOIN departments d
ON e.dept_id = d.id;
```

---

<a id="q16"></a>

## 16. Left join concept

```sql
SELECT *
FROM employees e
LEFT JOIN departments d
ON e.dept_id = d.id;
```

---

<a id="q17"></a>

## 17. Find max salary

```sql
SELECT MAX(salary) FROM employees;
```

---

<a id="q18"></a>

## 18. Find min salary

```sql
SELECT MIN(salary) FROM employees;
```

---

<a id="q19"></a>

## 19. Employees with salary between range

```sql
SELECT * FROM employees
WHERE salary BETWEEN 30000 AND 60000;
```

---

<a id="q20"></a>

## 20. Find duplicates in a column

```sql
SELECT name, COUNT(*)
FROM employees
GROUP BY name
HAVING COUNT(*) > 1;
```
## 21. Write a solution to find the employees who earn more than their managers.

```sql
select e.name as Employee
from Employee e join Employee m 
on e.managerID= m.managerID
where e.salary> m.salary()
```
## 22. Write a solution to delete all duplicate emails, keeping only one unique email with the smallest id.

```sql
delete p2
from person p1, person p2
where p1.email= p2.email 
      and p1.id<p2.id;
```
