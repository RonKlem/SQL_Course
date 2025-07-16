# 10-Minute SQL Crash Course

## Agenda

- Introduce SQL and relational tables  
- Write your first SELECT query  
- Filter results with WHERE  
- Sort results with ORDER BY  
- Quick hands-on exercise  

---

## 1. What Is SQL?

SQL (Structured Query Language) lets you interact with relational databases.  

You use SQL to retrieve, insert, update, and delete data.  

Today we’ll focus on reading data: the SELECT statement.  

---

## 2. Basic Query Structure

Every SELECT query follows this pattern:

```sql
SELECT column1, column2
FROM table_name
WHERE condition
ORDER BY column1 [ASC|DESC];
```

- SELECT specifies which columns you want.  
- FROM names the table.  
- WHERE filters rows.  
- ORDER BY sorts the output.  

---

## 3. Sample Table: employees

| employee_id | first_name | last_name | department | salary |
|-------------|------------|-----------|------------|-------:|
| 1           | Alice      | Jones     | Sales      |  55000 |
| 2           | Bob        | Smith     | Marketing  |  62000 |
| 3           | Carol      | Lee       | Sales      |  58000 |
| 4           | Dan        | Patel     | Engineering|  75000 |
| 5           | Erin       | Wong      | Marketing  |  60000 |

---

## 4. Write and Run Your First Query

1. Show all columns:  
   ```sql
   SELECT * 
   FROM employees;
   ```

2. Select specific columns:  
   ```sql
   SELECT first_name, salary 
   FROM employees;
   ```

---

## 5. Filter and Sort

- Filter to only Sales:  
  ```sql
  SELECT * 
  FROM employees 
  WHERE department = 'Sales';
  ```

- Then sort by salary descending:  
  ```sql
  SELECT first_name, last_name, salary 
  FROM employees 
  WHERE department = 'Sales' 
  ORDER BY salary DESC;
  ```

---

## 6. Hands-On Exercise (5 minutes)

Ask each person to write a query that:

- Selects first_name, last_name, department  
- Filters for salary > 60000  
- Orders by last_name ascending  

Share queries and results in your SQL client.  

Let’s walk through the hands-on exercise step by step.

### 🧪 Exercise Prompt:
> Write a query that:
> - Selects `first_name`, `last_name`, `department`  
> - Filters for `salary > 60000`  
> - Orders by `last_name` ascending  

### ✅ Correct SQL Query:
```sql
SELECT first_name, last_name, department
FROM employees
WHERE salary > 60000
ORDER BY last_name ASC;
```

### 📊 Expected Output (based on sample data):

| first_name | last_name | department   |
|------------|-----------|--------------|
| Dan        | Patel     | Engineering  |
| Bob        | Smith     | Marketing    |
| Erin       | Wong      | Marketing    |

These are the employees with salaries over 60,000, sorted alphabetically by last name.

---

## Next Steps

After mastering SELECT, explore:

- Aggregations with SUM, AVG, COUNT  
- GROUP BY and HAVING clauses  
- Joining multiple tables  
- Creating and indexing tables  

These topics build on today’s foundation.
