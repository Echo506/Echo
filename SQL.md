# 📋 **Note:**

My purpose with this Python course is to start from the very basics, so that those who are new to the field can acquire their first knowledge and progress to developing their own projects. It's always valuable to review the fundamentals, and in the process, one often ends up learning something new.

---

# **Transact-SQL (T-SQL)**

## **What is Transact-SQL (T-SQL)?**

Transact-SQL (T-SQL) is Microsoft's proprietary extension to **Structured Query Language (SQL)**. It is fundamental for:

* **Querying, managing, and manipulating relational databases** within Microsoft SQL Server.

T-SQL includes:

* **Standard SQL syntax** (`SELECT`, `INSERT`, `UPDATE`, `DELETE`, etc.)
* **Control-of-flow language** (`IF`, `WHILE`, `BEGIN...END`, `GOTO`)
* **Error handling** (`TRY...CATCH`)
* **Variables and functions**
* **Transactions**

---

## **Core Categories of T-SQL Commands**

### **Data Definition Language (DDL)**

DDL commands are used to **define or modify the database structure**.

| Command    | Description                                       |
| :--------- | :------------------------------------------------ |
| `CREATE`   | Creates a new object (table, view, index, etc.)   |
| `ALTER`    | Modifies an existing database object              |
| `DROP`     | Deletes an object from the database               |
| `TRUNCATE` | Deletes all data from a table (faster than `DELETE`) |

**Example:**

```sql
-- Create a new table
CREATE TABLE Employees (
    ID INT PRIMARY KEY,
    Name NVARCHAR(100),
    Position NVARCHAR(50),
    Salary DECIMAL(10,2)
);

-- Alter an existing table by adding a new column
ALTER TABLE Employees ADD Department NVARCHAR(50);

-- Drop a table
DROP TABLE Employees;
````

-----

### **Data Manipulation Language (DML)**

DML commands are used to **manage data within database objects**.

| Command  | Description             |
| :------- | :---------------------- |
| `SELECT` | Retrieves data          |
| `INSERT` | Adds new records        |
| `UPDATE` | Modifies existing records |
| `DELETE` | Removes records         |

**Examples:**

```sql
-- Insert data into the Employees table
INSERT INTO Employees (ID, Name, Position, Salary)
VALUES (1, 'John Smith', 'Manager', 75000.00);

-- Select all data from the Employees table
SELECT * FROM Employees;

-- Update data for an existing record
UPDATE Employees
SET Salary = 80000
WHERE ID = 1;

-- Delete data from a table
DELETE FROM Employees WHERE ID = 1;
```

-----

### **Data Control Language (DCL)**

DCL commands are used to **manage permissions and access rights** to the database.

| Command  | Description           |
| :------- | :-------------------- |
| `GRANT`  | Gives user privileges |
| `REVOKE` | Removes user privileges |

**Example:**

```sql
-- Grant SELECT and INSERT permissions on the Employees table to 'User1'
GRANT SELECT, INSERT ON Employees TO User1;

-- Revoke INSERT permission on the Employees table from 'User1'
REVOKE INSERT ON Employees FROM User1;
```

-----

### **Transaction Control Language (TCL)**

TCL commands are used to **manage transactions within a database**.

| Command           | Description        |
| :---------------- | :----------------- |
| `BEGIN TRANSACTION` | Starts a transaction |
| `COMMIT`          | Saves changes      |
| `ROLLBACK`        | Reverts changes    |

**Example:**

```sql
-- Start a new transaction
BEGIN TRANSACTION;

-- Update all employees' salaries by 10%
UPDATE Employees SET Salary = Salary * 1.1;

-- If all operations within the transaction are successful, commit the changes
COMMIT;

-- If an error occurs, revert all changes made within the transaction
-- ROLLBACK;
```

-----

### **Control-of-Flow Language**

T-SQL includes constructs for **controlling the flow of execution**.

| Command     | Description           |
| :---------- | :-------------------- |
| `IF...ELSE` | Conditional execution |
| `WHILE`     | Loop execution        |
| `GOTO`      | Jumps to a label      |
| `RETURN`    | Exits a procedure     |

**Example:**

```sql
-- Conditional statement example
DECLARE @Age INT = 25;

IF @Age >= 18
    PRINT 'Adult';
ELSE
    PRINT 'Minor';

-- Loop example
DECLARE @i INT = 1;
WHILE @i <= 5
BEGIN
    PRINT 'Number: ' + CAST(@i AS VARCHAR);
    SET @i = @i + 1;
END;
```

-----

### **Variables and Functions**

#### **Declaring and Using Variables**

Variables are used to store data temporarily within T-SQL batches or scripts.

```sql
-- Declare a variable named @Name with NVARCHAR(100) data type
DECLARE @Name NVARCHAR(100);
-- Set the value of the @Name variable
SET @Name = 'Alice';

-- Print the variable's value
PRINT 'Hello, ' + @Name;
```

#### **Built-in Functions**

T-SQL offers a wide range of built-in functions for various operations.

| Function Type | Examples                                       |
| :------------ | :--------------------------------------------- |
| String        | `LEN()`, `UPPER()`, `LOWER()`, `SUBSTRING()`   |
| Math          | `ROUND()`, `CEILING()`, `FLOOR()`              |
| Date/Time     | `GETDATE()`, `DATEADD()`, `DATEDIFF()`         |
| Conversion    | `CAST()`, `CONVERT()`                          |

-----

### **Stored Procedures & Views**

#### **Stored Procedure**

A stored procedure is a **reusable block of T-SQL code** that performs a specific task. They enhance security and performance.

```sql
-- Create a stored procedure to get employee details by ID
CREATE PROCEDURE GetEmployeeById @ID INT
AS
BEGIN
    SELECT * FROM Employees WHERE ID = @ID;
END;
```

#### **View**

A view is a **virtual table** based on the result-set of a `SELECT` query. It does not store data itself but rather displays data from one or more underlying tables.

```sql
-- Create a view to show employees with a high salary
CREATE VIEW HighSalaryEmployees AS
SELECT Name, Salary FROM Employees
WHERE Salary > 50000;
```

-----

### **Joins and Subqueries**

#### **JOIN Types**

JOINs are used to combine rows from two or more tables, based on a related column between them.

  * `INNER JOIN`: Returns records that have matching values in both tables.
  * `LEFT JOIN`: Returns all records from the left table, and the matching records from the right table. If there is no match, the result is NULL from the right side.
  * `RIGHT JOIN`: Returns all records from the right table, and the matching records from the left table. If there is no match, the result is NULL from the left side.
  * `FULL JOIN`: Returns all records when there is a match in either left or right table records.

**Example:**

```sql
-- INNER JOIN to combine Employees and Departments tables
SELECT E.Name, D.Name AS Department
FROM Employees E
INNER JOIN Departments D ON E.DepartmentID = D.ID;
```

-----

## **Best Practices**

To ensure robust, secure, and efficient T-SQL development:

  * **Use `TRY...CATCH` blocks for robust error handling.**
  * **Employ parameterized queries to prevent SQL Injection vulnerabilities.**
  * **Keep transactions short to minimize locking and improve concurrency.**
  * **Index frequently queried columns to significantly enhance query performance.**

<!-- end list -->

```
```
