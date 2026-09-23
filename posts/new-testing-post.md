---
title: New Testing Post
description: Short description
for testing blogs
author: Arzzon
date: 2026-09-23T16:09:35.165Z
updated: 2026-09-23T16:09:35.165Z
tags: 
cover: ""
division: general
published: false
---

# SQL Practice Quiz — Part 2

**Questions 13–20**

> **Instructions:** Solve all questions on your own.  
> Write the SQL query when requested, and choose the correct answer when options are provided.  
> **Do not use the answers from the course or ask for help before trying each question.**

---

## Question 13 — LEFT JOIN

**Difficulty:** ⭐⭐⭐

You have the following tables:

### Students

| id | name |
|---:|---|
| 1 | Ali |
| 2 | Sara |
| 3 | Omar |

### Enrollments

| student_id | course |
|---:|---|
| 1 | SQL |
| 2 | Python |

You want to display **all students**, including students who are **not enrolled in any course**.

Which JOIN should you use?

**A.** `INNER JOIN`  
**B.** `LEFT JOIN`  
**C.** `RIGHT JOIN`  
**D.** `CROSS JOIN`

**Your Answer:** ____________________

---

## Question 14 — UPDATE

**Difficulty:** ⭐⭐

You want to increase the salary of the employee with `id = 5` by **500**.

Which query is correct?

**A**
```sql
UPDATE Employees
SET salary = salary + 500
WHERE id = 5;
```

**B**
```sql
UPDATE Employees
SET salary + 500
WHERE id = 5;
```

**C**
```sql
UPDATE Employees
WHERE id = 5
SET salary = salary + 500;
```

**D**
```sql
UPDATE salary
FROM Employees
SET salary = salary + 500
WHERE id = 5;
```

**Your Answer:** ____________________

---

## Question 15 — DELETE

**Difficulty:** ⭐⭐⭐

You want to delete **only the employee whose ID is 10**.

Which query is safest?

**A**
```sql
DELETE Employees;
```

**B**
```sql
DELETE FROM Employees
WHERE id = 10;
```

**C**
```sql
DELETE id = 10 FROM Employees;
```

**D**
```sql
REMOVE FROM Employees
WHERE id = 10;
```

**Your Answer:** ____________________

---

## Question 16 — Primary Key

**Difficulty:** ⭐⭐

Which statement about a `PRIMARY KEY` is correct?

**A.** It can contain duplicate values.

**B.** It can contain multiple `NULL` values.

**C.** It uniquely identifies each row.

**D.** It is only used for sorting data.

**Your Answer:** ____________________

---

## Question 17 — Foreign Key

**Difficulty:** ⭐⭐⭐

You have:

```text
Customers
-----------
customer_id
name
```

and:

```text
Orders
-----------
order_id
customer_id
total
```

What should `Orders.customer_id` normally be?

**A.** Primary Key only

**B.** Foreign Key referencing `Customers.customer_id`

**C.** Foreign Key referencing `Orders.order_id`

**D.** It cannot be related to another table

**Your Answer:** ____________________

---

## Question 18 — Predict the Result

**Difficulty:** ⭐⭐⭐

Table: `Products`

| name | price |
|---|---:|
| Laptop | 1000 |
| Mouse | 20 |
| Keyboard | 50 |
| Monitor | 300 |

What will this query return?

```sql
SELECT name
FROM Products
WHERE price > 20
ORDER BY price ASC;
```

**A**
```text
Laptop
Monitor
Keyboard
```

**B**
```text
Keyboard
Monitor
Laptop
```

**C**
```text
Mouse
Keyboard
Monitor
Laptop
```

**D**
```text
Laptop
Keyboard
Monitor
```

**Your Answer:** ____________________

---

## Question 19 — GROUP BY + HAVING

**Difficulty:** ⭐⭐⭐⭐

Table: `Orders`

| order_id | customer | total |
|---:|---|---:|
| 1 | Ali | 100 |
| 2 | Sara | 250 |
| 3 | Ali | 150 |
| 4 | Omar | 80 |
| 5 | Sara | 100 |

Which query finds customers whose **total orders value is greater than 200**?

**A**
```sql
SELECT customer, SUM(total)
FROM Orders
WHERE total > 200
GROUP BY customer;
```

**B**
```sql
SELECT customer, SUM(total)
FROM Orders
GROUP BY customer
HAVING SUM(total) > 200;
```

**C**
```sql
SELECT customer, SUM(total)
FROM Orders
WHERE SUM(total) > 200
GROUP BY customer;
```

**D**
```sql
SELECT customer, total
FROM Orders
GROUP BY customer
HAVING total > 200;
```

**Your Answer:** ____________________

---

## Question 20 — Multiple JOINs

**Difficulty:** ⭐⭐⭐⭐

You have the following tables:

### Students

| id | name |
|---:|---|
| 1 | Ali |
| 2 | Sara |
| 3 | Omar |

### Courses

| id | course_name |
|---:|---|
| 10 | SQL |
| 20 | Python |

### Enrollments

| student_id | course_id |
|---:|---:|
| 1 | 10 |
| 1 | 20 |
| 2 | 10 |

You want to display:

```text
Ali - SQL
Ali - Python
Sara - SQL
```

Which query is correct?

**A**
```sql
SELECT Students.name, Courses.course_name
FROM Students
JOIN Courses
ON Students.id = Courses.id;
```

**B**
```sql
SELECT Students.name, Courses.course_name
FROM Students
JOIN Enrollments
ON Students.id = Enrollments.student_id
JOIN Courses
ON Enrollments.course_id = Courses.id;
```

**C**
```sql
SELECT Students.name, Courses.course_name
FROM Students
JOIN Enrollments
ON Students.id = Courses.id
JOIN Courses
ON Enrollments.course_id = Students.id;
```

**D**
```sql
SELECT Students.name, Courses.course_name
FROM Students, Courses
WHERE Students.id = Courses.id;
```

**Your Answer:** ____________________

---

# Bonus Challenge — Write SQL

**Difficulty:** ⭐⭐⭐⭐

This question is not multiple choice.

You have:

### Employees

| id | name | department | salary |
|---:|---|---|---:|
| 1 | Ali | IT | 2000 |
| 2 | Sara | HR | 3000 |
| 3 | Omar | IT | 3500 |
| 4 | Lina | HR | 4000 |
| 5 | Ahmad | Sales | 2500 |

Write **one SQL query** that displays the departments whose **average salary is greater than 2500**, showing:

- Department name
- Average salary

Expected format:

```text
HR    3500
IT    2750
```

**Your SQL:**

```sql

```

---

# Bonus Challenge 2 — Think Carefully

**Difficulty:** ⭐⭐⭐⭐

Using the same `Employees` table, write a query that displays the employees whose salary is **higher than the average salary of all employees**.

**Your SQL:**

```sql

```

> Take your time. This question requires you to think about how to compare each employee's salary with a calculated value.
