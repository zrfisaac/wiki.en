# SQLite

This guide provides information on how to work with SQLite, including common query examples, best practices, and tips for database management. Whether you're a beginner or an experienced user, this guide will help you get the most out of SQLite.

## Table of Contents

- [Introduction to SQLite](#introduction-to-sqlite)  
  Overview of SQLite, its features, and how to set it up.

- [Connecting to SQLite Database](#connecting-to-sqlite-database)  
  How to establish a connection to an SQLite database using different methods.

- [Basic SQL Queries in SQLite](#basic-sql-queries-in-sqlite)  
  Common SQL queries in SQLite, including selecting, inserting, updating, and deleting data.

- [Advanced Queries and Functions](#advanced-queries-and-functions)  
  Advanced SQL operations such as joins, subqueries, and triggers in SQLite.

- [Performance Optimization](#performance-optimization)  
  Tips for optimizing your SQLite database performance.

- [Error Handling and Debugging](#error-handling-and-debugging)  
  How to handle errors and debug SQL queries in SQLite.

---

## Introduction to SQLite

SQLite is a self-contained, serverless, and zero-configuration SQL database engine. Unlike other database management systems (DBMS), SQLite does not require a separate server process, and the database is stored as a single file on disk. This makes SQLite ideal for embedded applications, local storage, or small-scale databases.

### Key Features of SQLite:
- Serverless and self-contained.
- Simple setup with no configuration required.
- Cross-platform and widely supported.
- Suitable for embedded systems, mobile apps, and small-scale applications.
- Supports most of the SQL-92 standard.

---

## Connecting to SQLite Database

To connect to an SQLite database, you can use libraries and tools depending on the programming language you're using.

### Example using **Python** with SQLite3:
```python
import sqlite3

# Connecting to SQLite database
connection = sqlite3.connect('example.db')

# Creating a cursor object to execute SQL queries
cursor = connection.cursor()
```

### Example using **SQLite Command Line**:
1. Open your terminal or command prompt.
2. Run the following command to open the SQLite command-line interface:
   ```bash
   sqlite3 example.db
   ```
3. You can now run SQL queries directly in the command line.

---

## Basic SQL Queries in SQLite

Here are some examples of common SQL queries you can use in SQLite.

### Selecting Data
To retrieve data from a table:

```sql
SELECT * FROM employees WHERE department = 'IT';
```

### Inserting Data
To insert a new record into a table:

```sql
INSERT INTO employees (id, name, department, salary) 
VALUES (1, 'John Doe', 'HR', 50000);
```

### Updating Data
To update an existing record:

```sql
UPDATE employees 
SET salary = 55000 
WHERE id = 1;
```

### Deleting Data
To delete a record:

```sql
DELETE FROM employees WHERE id = 1;
```

---

## Advanced Queries and Functions

### Joins
SQLite supports `INNER JOIN`, `LEFT JOIN`, and `CROSS JOIN`. Here's an example of an `INNER JOIN`:

```sql
SELECT e.name, d.name 
FROM employees e
INNER JOIN departments d ON e.department_id = d.id;
```

### Subqueries
Subqueries can be used to retrieve data that will be used by another query. Example:

```sql
SELECT name FROM employees
WHERE salary > (SELECT AVG(salary) FROM employees);
```

### Creating Triggers
Triggers are used to perform actions automatically when certain events occur, such as insertions, updates, or deletions.

```sql
CREATE TRIGGER before_employee_update
BEFORE UPDATE ON employees
FOR EACH ROW
BEGIN
    INSERT INTO audit_log (action, employee_id) 
    VALUES ('Updated', OLD.id);
END;
```

### Creating Views
You can create views in SQLite to simplify complex queries:

```sql
CREATE VIEW employee_summary AS
SELECT id, name, department, salary FROM employees WHERE salary > 40000;
```

---

## Performance Optimization

SQLite is designed to be efficient for most use cases, but there are some techniques you can use to improve performance:

- **Use Transactions**: Grouping multiple queries within a single transaction can significantly speed up operations.
  
```sql
BEGIN TRANSACTION;
UPDATE employees SET salary = salary + 500 WHERE department = 'IT';
INSERT INTO employees (id, name, department, salary) VALUES (2, 'Jane Smith', 'Sales', 48000);
COMMIT;
```

- **Indexing**: Create indexes on columns that are frequently used in `WHERE`, `JOIN`, or `ORDER BY` clauses.
  
```sql
CREATE INDEX idx_employee_department 
ON employees(department);
```

- **Use `EXPLAIN`**: The `EXPLAIN` command can help you analyze the query execution plan and improve performance.
  
```sql
EXPLAIN QUERY PLAN SELECT * FROM employees WHERE department = 'IT';
```

---

## Error Handling and Debugging

SQLite provides basic error handling capabilities through the `sqlite3_errmsg()` function or by checking the return codes of SQL queries. For most programming languages, error handling is done through exceptions.

### Example in **Python**:

```python
try:
    cursor.execute("SELECT * FROM employees WHERE department = 'IT'")
except sqlite3.DatabaseError as e:
    print(f"Database error: {e}")
```

SQLite also supports the `ROLLBACK` command to revert changes made during a transaction if an error occurs.

```sql
BEGIN TRANSACTION;
UPDATE employees SET salary = salary + 500 WHERE department = 'HR';
-- If an error occurs, we can revert the changes
ROLLBACK;
```
