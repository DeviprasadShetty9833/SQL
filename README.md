# SQL

<br> ![Author: Deviprasad Shetty](https://img.shields.io/badge/Author-💫_Deviprasad%20Shetty-000000?style=for-the-badge&labelColor=white)
 
| [![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5?style=for-the-badge&logo=LinkedIn&logoColor=white)](https://linkedin.com/in/deviprasad-shetty-4bba49313) | [![My_Portfolio](https://img.shields.io/badge/My_Portfolio-indigo?style=for-the-badge&logo=firefox&logoColor=white)](https://deviprasadshetty.com/) | [![My_Projects](https://img.shields.io/badge/My_Projects-000?style=for-the-badge&logo=GitHub&logoColor=white)](https://github.com/DeviprasadShetty9833/My_Projects)  |                      
|---|---|---|

---

Full MySQL Command Arsenal ⚔️

✨ Each command includes general syntax, practical example, and clear explanation for easy understanding!

---

Here are comprehensive SQL fundamentals with examples and explanations following your requested format:

---

## **1. Creates a new database**
```sql
CREATE DATABASE database_name;
```

*Example:*
```sql
CREATE DATABASE company;
```

*Explanation:*
Creates a new database named 'company' where you can store tables and data.

---

## **2. Selects a database to use**
```sql
USE database_name;
```

*Example:*
```sql
USE company;
```

*Explanation:*
Switches to the 'company' database context. All subsequent operations will be performed on this database.

---

## **3. Creates a new table**
```sql
CREATE TABLE table_name (
    column1 datatype constraints,
    column2 datatype constraints
);
```

*Example:*
```sql
CREATE TABLE employees (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(50) NOT NULL,
    salary DECIMAL(10,2),
    hire_date DATE
);
```

*Explanation:*
Creates a table called 'employees' with columns for ID, name, salary, and hire date. ID is the primary key that auto-increments.

---

## **4. Inserts data into a table**
```sql
INSERT INTO table_name (column1, column2) VALUES (value1, value2);
```

*Example:*
```sql
INSERT INTO employees (name, salary, hire_date) 
VALUES ('John Doe', 50000.00, '2023-01-15');
```

*Explanation:*
Adds a new employee record with name 'John Doe', salary 50000, and hire date January 15, 2023.

---

## **5. Retrieves data from a table**
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```

*Example:*
```sql
SELECT name, salary FROM employees WHERE salary > 40000;
```

*Explanation:*
Fetches names and salaries of all employees earning more than 40,000.

---

## **6. Updates existing records**
```sql
UPDATE table_name SET column1 = value1 WHERE condition;
```

*Example:*
```sql
UPDATE employees SET salary = 55000 WHERE name = 'John Doe';
```

*Explanation:*
Increases John Doe's salary to 55,000 in the employees table.

---

## **7. Deletes records from a table**
```sql
DELETE FROM table_name WHERE condition;
```

*Example:*
```sql
DELETE FROM employees WHERE hire_date < '2020-01-01';
```

*Explanation:*
Removes all employees who were hired before January 1, 2020.

---

## **8. Adds a new column to table**
```sql
ALTER TABLE table_name ADD column_name datatype;
```

*Example:*
```sql
ALTER TABLE employees ADD department VARCHAR(30);
```

*Explanation:*
Adds a new 'department' column to the existing employees table to store department names.

---

## **9. Modifies column datatype**
```sql
ALTER TABLE table_name MODIFY column_name new_datatype;
```

*Example:*
```sql
ALTER TABLE employees MODIFY salary DECIMAL(12,2);
```

*Explanation:*
Changes the salary column to allow larger values (up to 12 digits with 2 decimal places).

---

## **10. Removes a table completely**
```sql
DROP TABLE table_name;
```

*Example:*
```sql
DROP TABLE temporary_data;
```

*Explanation:*
Permanently deletes the 'temporary_data' table and all its data from the database.

---

## **11. Creates an index for faster queries**
```sql
CREATE INDEX index_name ON table_name (column_name);
```

*Example:*
```sql
CREATE INDEX idx_employee_name ON employees (name);
```

*Explanation:*
Creates an index on the name column to speed up search operations involving employee names.

---

## **12. Combines rows from multiple tables**
```sql
SELECT columns FROM table1 JOIN table2 ON table1.column = table2.column;
```

*Example:*
```sql
SELECT employees.name, departments.dept_name 
FROM employees 
JOIN departments ON employees.dept_id = departments.id;
```

*Explanation:*
Retrieves employee names along with their department names by joining employees and departments tables.

---

## **13. Groups rows and applies aggregate functions**
```sql
SELECT column, COUNT(*) FROM table_name GROUP BY column;
```

*Example:*
```sql
SELECT department, COUNT(*) as employee_count 
FROM employees 
GROUP BY department;
```

*Explanation:*
Counts how many employees work in each department by grouping records by department.

---

## **14. Filters groups with HAVING clause**
```sql
SELECT column, COUNT(*) FROM table_name GROUP BY column HAVING condition;
```

*Example:*
```sql
SELECT department, AVG(salary) as avg_salary 
FROM employees 
GROUP BY department 
HAVING AVG(salary) > 50000;
```

*Explanation:*
Shows only departments where the average salary is greater than 50,000.

---

## **15. Removes a database completely**
```sql
DROP DATABASE database_name;
```

*Example:*
```sql
DROP DATABASE old_company;
```

*Explanation:*
Permanently deletes the entire 'old_company' database and all its contents.

---

| [![TOP](https://img.shields.io/badge/_🔺_-Navigate_to_TOP_↑_-blue?style=for-the-badge&labelColor=white)](#SQL) | [![My_Portfolio](https://img.shields.io/badge/Back_to-My_Portfolio-indigo?style=for-the-badge&logo=firefox&logoColor=white)](https://deviprasadshetty.com/) |  [![LinkedIn](https://img.shields.io/badge/Back_to-LinkedIn-%230077B5?style=for-the-badge&logo=LinkedIn&logoColor=white)](https://linkedin.com/in/deviprasad-shetty-4bba49313) |
|---|---|---|
