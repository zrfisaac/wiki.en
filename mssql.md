# SQL Server

This guide provides information on how to work with SQL Server, including common query examples, best practices, and tips for optimizing database performance. Whether you're a beginner or an experienced user, this guide will help you get the most out of SQL Server.

## Table of Contents

- [Introduction to SQL Server](#introduction-to-sql-server)  
  Overview of SQL Server, its features, and how to set it up.

- [Connecting to SQL Server Database](#connecting-to-sql-server-database)  
  How to establish a connection to an SQL Server database using various methods.

- [Basic SQL Queries in SQL Server](#basic-sql-queries-in-sql-server)  
  Common SQL queries in SQL Server, including selecting, inserting, updating, and deleting data.

- [Advanced Queries and Functions](#advanced-queries-and-functions)  
  Advanced SQL operations, such as joins, subqueries, triggers, and stored procedures.

- [Performance Optimization](#performance-optimization)  
  Tips for optimizing your SQL Server database performance.

- [Error Handling and Debugging](#error-handling-and-debugging)  
  How to handle errors and debug SQL queries in SQL Server.

---

## Introduction to SQL Server

SQL Server is a relational database management system (RDBMS) developed by Microsoft. It offers advanced features such as transactions, security, high availability, and support for unstructured data. SQL Server is widely used in enterprises for mission-critical systems.

### Key Features of SQL Server:
- ACID-compliant transactions.
- Enterprise-grade security.
- Support for Big Data and parallel processing.
- Advanced analytics and reporting tools.
- Scalability and high availability.

---

## Connecting to SQL Server Database

To connect to an SQL Server database, you can use various methods depending on the platform and technology you're working with.

### Example using **ADO.NET** in C#:
```csharp
using System.Data.SqlClient;

string connectionString = "Server=localhost;Database=MyDatabase;User Id=user;Password=password;";
SqlConnection connection = new SqlConnection(connectionString);
connection.Open();
```

### Example using **SQL Server Management Studio (SSMS)**:
1. Open SSMS.
2. Enter the server name, database, and credentials.
3. Click "Connect" to access the database.

---

## Basic SQL Queries in SQL Server

Here are some examples of common SQL queries that you can use in SQL Server.

### Selecting Data
To retrieve data from a table:

```sql
SELECT * FROM employees WHERE department = 'IT';
```

### Inserting Data
To add a new record into a table:

```sql
INSERT INTO employees (id, name, department, salary) 
VALUES (1, 'Maria Oliveira', 'IT', 45000);
```

### Updating Data
To modify an existing record:

```sql
UPDATE employees 
SET salary = 48000 
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
SQL Server supports various types of joins, such as `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`, and `FULL JOIN`. Example of an `INNER JOIN`:

```sql
SELECT e.name, d.name
FROM employees e
INNER JOIN departments d ON e.department_id = d.id;
```

### Subqueries
Subqueries can be used to return data that will be used in another query. Example:

```sql
SELECT name FROM employees 
WHERE salary > (SELECT AVG(salary) FROM employees);
```

### Creating Triggers
Triggers are used to perform actions automatically when specific events occur, such as insertions or updates.

```sql
CREATE TRIGGER trg_salary 
ON employees
AFTER UPDATE
AS
BEGIN
  IF UPDATE(salary)
  BEGIN
    PRINT 'Salary updated!';
  END
END;
```

### Stored Procedures
Stored procedures help encapsulate business logic in the database.

```sql
CREATE PROCEDURE IncreaseSalary
    @EmployeeId INT,
    @Increment FLOAT
AS
BEGIN
    UPDATE employees
    SET salary = salary + @Increment
    WHERE id = @EmployeeId;
END;
```

---

## Performance Optimization

SQL Server performance can be improved by following best practices and techniques. Here are some tips:

- **Indexing**: Create indexes on columns frequently used in `WHERE`, `JOIN`, or `ORDER BY` conditions.
- **Execution Plans**: Use the **Execution Plan** to check the efficiency of your queries.
- **Avoid Unnecessary Subqueries**: Use joins and CTEs instead of subqueries when possible.
- **Update Statistics**: Keep your database statistics up to date to improve query performance.
  
Example of creating an index:

```sql
CREATE INDEX idx_employee_department 
ON employees(department);
```

---

## Error Handling and Debugging

SQL Server provides various tools for error handling, such as the **TRY...CATCH** block. Example:

```sql
BEGIN TRY
    -- Code that might generate an error
    UPDATE employees SET salary = salary + 500 WHERE id = 1;
END TRY
BEGIN CATCH
    -- Error handling code
    PRINT 'Error: ' + ERROR_MESSAGE();
END CATCH;
```

You can also use the `RAISEERROR` command to generate custom error messages.

```sql
RAISEERROR('An error occurred during the update process!', 16, 1);
```

By following these practices, you can ensure that your SQL Server database runs efficiently and securely.
