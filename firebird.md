# Firebird

This guide provides essential information on how to interact with Firebird SQL, including examples of common queries, tips for performance optimization, and best practices for working with the database. Whether you're a beginner or an experienced developer, this guide will help you get the most out of your Firebird database.

## Table of Contents

- [Introduction to Firebird SQL](#introduction-to-firebird-sql)  
  An overview of Firebird SQL, its features, and how to set it up.

- [Connecting to Firebird Database](#connecting-to-firebird-database)  
  How to establish a connection to a Firebird database using different methods.

- [Basic SQL Queries in Firebird](#basic-sql-queries-in-firebird)  
  Common SQL queries for Firebird, including selecting, inserting, updating, and deleting data.

- [Advanced Queries and Functions](#advanced-queries-and-functions)  
  Advanced SQL operations such as joins, subqueries, triggers, and stored procedures.

- [Performance Optimization](#performance-optimization)  
  Tips and best practices for optimizing the performance of your Firebird database.

- [Error Handling and Debugging](#error-handling-and-debugging)  
  How to handle errors and debug issues with Firebird SQL queries.

---

## Introduction to Firebird SQL

Firebird SQL is a powerful, open-source relational database management system (RDBMS) known for its high performance, small footprint, and easy deployment. It supports standard SQL as well as advanced features like stored procedures, triggers, and user-defined functions. 

### Features of Firebird SQL:
- Cross-platform (Linux, Windows, macOS).
- ACID compliant for reliable transactions.
- Support for complex queries and indexing.
- Stored procedures, triggers, and user-defined functions.
- Efficient handling of multi-user environments.

---

## Connecting to Firebird Database

To connect to a Firebird database, you need to use a connection string that specifies the database file location and other connection details. 

### Example using **FireDAC** in Delphi:
```delphi
FDConnection1.Params.Add('DriverID=FB');
FDConnection1.Params.Add('Database=C:\path\to\your\database.fdb');
FDConnection1.Connected := True;
```

### Example using **ADO** in C#:
```csharp
using System.Data.OleDb;

string connectionString = "Provider=FirebirdOLEDB;Data Source=localhost;Database=C:\\path\\to\\your\\database.fdb;";
OleDbConnection connection = new OleDbConnection(connectionString);
connection.Open();
```

---

## Basic SQL Queries in Firebird

Here are some common SQL queries to help you interact with your Firebird database.

### Selecting Data
To retrieve data from a table:

```sql
SELECT * FROM employees WHERE department = 'Sales';
```

### Inserting Data
To add a new row into a table:

```sql
INSERT INTO employees (id, name, department, salary) 
VALUES (1, 'John Doe', 'Sales', 50000);
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
Firebird SQL supports several types of joins, including `INNER JOIN`, `LEFT JOIN`, and `RIGHT JOIN`. Here's an example of an inner join:

```sql
SELECT e.name, d.name
FROM employees e
INNER JOIN departments d ON e.department_id = d.id;
```

### Subqueries
A subquery is a query nested inside another query. Example:

```sql
SELECT name FROM employees 
WHERE salary > (SELECT AVG(salary) FROM employees);
```

### Creating Triggers
Triggers are used to automatically execute a set of actions when certain events occur, like insertions or updates.

```sql
CREATE TRIGGER update_employee_salary
FOR employees
ACTIVE BEFORE UPDATE
AS
BEGIN
  IF (NEW.salary > OLD.salary) THEN
    INSERT INTO salary_changes (employee_id, old_salary, new_salary) 
    VALUES (NEW.id, OLD.salary, NEW.salary);
END;
```

### Stored Procedures
Stored procedures are useful for encapsulating business logic and performing more complex operations.

```sql
SET TERM ^ ;
CREATE PROCEDURE increase_salary (emp_id INT, increment FLOAT)
AS
BEGIN
  UPDATE employees 
  SET salary = salary + increment 
  WHERE id = emp_id;
END;
^
SET TERM ; ^
```
