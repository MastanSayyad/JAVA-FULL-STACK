**MySQL Notes**

## Learning SQL roadmap (step-by-step) FOR INTERVIEW

- [x] 1. [SQL. MySQL, DB, DBMS](https://github.com/MastanSayyad/JAVA-FULL-STACK/blob/main/SQL.md#sql)
- [x] 2. [Difference between SQL and MySQL](https://github.com/MastanSayyad/JAVA-FULL-STACK/blob/main/SQL.md#sql-and-mysql)
- [x] 3. [RDBMS, Table, How to Create Database](https://github.com/MastanSayyad/JAVA-FULL-STACK/blob/main/SQL.md#rdbms-relational-mysql)
- [x] 4. [How to create database and common commands)](https://github.com/MastanSayyad/JAVA-FULL-STACK/blob/main/SQL.md#how-to-create-database)
- [x] 5. [Types of Commands: DDL, DML, DQL, DCL, TCL](https://github.com/MastanSayyad/JAVA-FULL-STACK/blob/main/SQL.md#types-of-sql-commands)
- [x] 6. [Data Types in SQL](https://github.com/MastanSayyad/JAVA-FULL-STACK/blob/main/SQL.md#datatypes-in-sql)
- [x] 7. [Constraints](https://github.com/MastanSayyad/JAVA-FULL-STACK/blob/main/SQL.md#constraints)
- [x] 7. [Operators in SQL](https://github.com/MastanSayyad/JAVA-FULL-STACK/blob/main/SQL.md#operators-in-sql)
- [x] 8. [Clauses in SQL Filtering (WHERE), sorting (ORDER BY), limiting (LIMIT)](https://github.com/MastanSayyad/JAVA-FULL-STACK/blob/main/SQL.md#clauses-in-sql)
- [x] 8. [Execution Flow order of SQL Commands](https://github.com/MastanSayyad/JAVA-FULL-STACK/blob/main/SQL.md#execution-flow-of-sql-commands)
- [ ] 9. Aggregation (COUNT, SUM, AVG, GROUP BY, HAVING)
- [ ] 10. Joins (INNER, LEFT, RIGHT, CROSS)
- [ ] 11. Subqueries & derived tables
- [ ] 12. indexes, keys (PK, FK)normalization
- [ ] 13. Transactions & ACID (BEGIN/COMMIT/ROLLBACK)
- [ ] 14. Views, stored procedures, functions, triggers (MySQL)
- [ ] 15. JDBC
- [ ] 16. Performance: EXPLAIN, indexes, query tuning
- [ ] 17. Security: users, privileges (GRANT/REVOKE) + backup basics

---

## SQL

SQL (Structured Query Language) is a standard language for storing, manipulating, and retrieving data in databases.

- **Data:** Raw facts and figures that have no meaning e.g `name, mastan, my, is`
  
- **Information:** Processed or organized data that gives meaning. e.g. `My Name is Mastan`
- **database:** A collection of related data organized in a structured way so it can be easily accessed, managed, and updated. e.g. `Table of fields and records`
- **DATABASE MANAGEMENT SYSTEM (DBMS):** It is a Software that helps you create, manage, and manipulate databases.
- **DATABASE SYSTEM (DBS):** DBS = Database + DBMS + Users + Applications
- **e.g.** MS Access, Oracle, MySQL, PostgreSQL, MongoDB

### Main Functions of a DBMS:
- Store data
- Retrieve data (when you search or query)
- Update/Delete data
- Secure data

## History (not imp)
- 1974 IBM - International Business Machines 
- 1979 Oracle - commercial sql -> RDBMS
- 1986 ANSI -
- 1990 -> my -> NoSQL, NongoDB

---

### SQL and MYSQL
- SQL: It is a Language used to interact with a database. **You use it to store, retrieve, update, or delete data.**
- MySQL: A popular open-source RDBMS that uses SQL as its language.

**MySQL Latest Version ->** 8.040v

## Difference between SQL and MYSQL (IMP Inteview)

 | **SQL**                                                            | **MySQL**                                                     |
 | ------------------------------------------------------------------ | ------------------------------------------------------------- |
 | SQL = Structured Query Language                                    | MySQL = A database software that uses SQL                     |
 | It’s a *language*                                                  | It’s a *database management system (DBMS)*                    |
 | Used to write commands to manage data                              | Stores and organizes data in tables                           |
 | Created by IBM; now an ISO/ANSI standard                           | Created by MySQL AB (now owned by Oracle)                     |
 | You use it to create, read, update, delete data (CRUD)             | You install and use it to actually store and retrieve data    | 
 | Concept / Standard                                                 | Practical software                                            |
 | `SELECT * FROM users;`                                             | You run that command *inside* MySQL                           |
 | Doesn’t store data itself                                          | Stores data in databases and tables                           |
 | Used by many systems (MySQL, SQL Server, Oracle, PostgreSQL, etc.) | One specific system that uses SQL                             |
 | Not software → no license                                          | Open-source (Community Edition) and paid (Enterprise Edition) | 
 | Depends on the DBMS that uses it                                   | Generally fast for read-heavy workloads                       |
 | SQL just defines commands                                          | MySQL provides user accounts, passwords, permissions          |
 | None (it’s only a language)                                        | Comes with tools like MySQL Workbench                         |
 | Describes *how* to query data                                      | Actually *stores and processes* the data                      |
 | Learn SQL once → use it anywhere                                   | Learn MySQL → works only for that system                      |

### Features of MYSQL
- High performance, availability
- Scalability and flexibility
- Robust and transactional
- strong data protecction
- Security and integrity

### Rules
- No spaces
- Start with letters
- **follow syntax**
- Avoid reserved words
- SQL is case-insensitive (e.g. Student, STUDENT are same)
- **SQL data is sensitive** (Tables and columns)

---

## RDBMS: relational MYSQL
- Data stored in the form of tables: rows and columns

**A TABLE:**
- A table is a structure in a database that organizes data into rows and columns.

**Example - Student Table:**

| student_id | name | age | city   |
| ---------- | ---- | --- | ------ |
| 1          | Mastan  | 22  | Bengaluru |
| 2          | Dhanraj | 23  | Pune   |
| 3          | Krupa | 22  | Delhi  |
| 4          | Pawan | 21  | Chennai  |
| 5          | Kavya | 21  | Hyderabad  |
| 6        | Rita | 20  | Nagpur  |


- **ROWS** = A **record** (also called a row or tuple)
- **Columns** =  A **field** (also called a column or attribute)

### Interview Easy to memorize:

| Term               | Meaning                      | Example                  |
| ------------------ | ---------------------------- | ------------------------ |
| **Table**          | Collection of rows & columns | Students                 |
| **Record (Row)**   | One complete data entry      | (1, 'Sam', 20, 'Mumbai') |
| **Field (Column)** | One type of data per record  | name, age, city          |

---

## How to create DATABASE:

Creating Databases:
- We can create database in mysql using create command:

```
CREATE DATABSE db_name;
```

- Delete or drop the database using:
  
```
DROP DATABASE db_name;
```
**Schema:**
- It is structure or architecture of the database
similarly in mysql we use schema (it is alternative name for database)

```
CREATE SCHEMA db_name;
```

To select the created database we use: `USE DATABASE statement`

```
use db_name;
```

- Delete or drop the database using:
  
```
DROP SCHEMA db_name;
```
- Create database when it does not exist in database

```
CREATE DATABASE IF NOT EXISTS db_name;
```

## QUICK Example of Database and table in SQL/MYSQL

```
CREATE DATABASE school;
USE school;

CREATE TABLE Students (
  student_id INT PRIMARY KEY,
  name VARCHAR(50),
  age INT,
  city VARCHAR(50)
);

INSERT INTO Students VALUES
(1, 'Sam', 20, 'Mumbai'),
(2, 'Rita', 21, 'Pune'),
(3, 'Amit', 22, 'Delhi');

SELECT * FROM Students;

```

**Output:**

| student_id | name | age | city   |
| ---------- | ---- | --- | ------ |
| 1          | Sam  | 20  | Mumbai |
| 2          | Rita | 21  | Pune   |
| 3          | Amit | 22  | Delhi  |

### Common SQL queries for database;
- `SHOW DATABASES;` It lists all databases in our system
- `SHOW TABLES;` It lists all tables we have in our use database
- `DESCRIBE table_name;` Show table structure (columns, types, keys)
- `DESC table_name;` Same as DESCRIBE
- `RENAME TABLE old_name TO new_name; ` It renames a table name

## Types of databse
1. Relational Database --> MySQL Oracle MS
2. Non relational: 
     - Analytical database  -->
     -  Key value  -->  Mongodb
     -  Column Family -->  

- CRUD is Basic operations on any database table.
- Create, Read, Update, Delete
- AS (Alias): In SQL, an alias is a temporary, alternative name given to a table or a column within a specific query.
- We cannot perform arithmetic operations on null

---

## Types of SQL Commands

| Type    | Full Form                    | Example                               |
| ------- | ---------------------------- | ------------------------------------- |
| **DDL** | Data Definition Language     | `CREATE`, `ALTER`, `DROP`, `TRUNCATE` |
| **DML** | Data Manipulation Language   | `INSERT`, `UPDATE`, `DELETE`          |
| **DQL** | Data Query Language          | `SELECT`                              |
| **DCL** | Data Control Language        | `GRANT`, `REVOKE`                     |
| **TCL** | Transaction Control Language | `COMMIT`, `ROLLBACK`, `SAVEPOINT`     |

---

### 1) DDL: Data Defination Lanaguage - it defines structure.

- **Structure / Design of the database (CREATE things)**
- once executed, can’t rollback.

| Command    | Meaning                               | Example                                             |
| ---------- | ------------------------------------- | --------------------------------------------------- |
| `CREATE`   | Make new table or database            | `CREATE TABLE students (id INT, name VARCHAR(50));` |
| `ALTER`    | Change structure (add/remove columns) | `ALTER TABLE students ADD age INT;`                 |
| `DROP`     | Delete table or database permanently  | `DROP TABLE students;`                              |
| `TRUNCATE` | Remove all data but keep structure    | `TRUNCATE TABLE students;`                          |
| `RENAME`   | Rename a table                        | `RENAME TABLE students TO learners;`                |


---

### 2) DML: Data Manipulation Language

- **Change or manipulate data inside tables**
- can ROLLBACK or COMMIT.

| Command  | Meaning                     | Example                                          |
| -------- | --------------------------- | ------------------------------------------------ |
| `INSERT` | Add new data                | `INSERT INTO students VALUES (1, 'Natsam', 22);` |
| `UPDATE` | Modify existing data        | `UPDATE students SET age = 23 WHERE id = 1;`     |
| `DELETE` | Delete data (not structure) | `DELETE FROM students WHERE id = 1;`             |

---

### 3) DQL - Data Query Language

- Fetch / read data

| Command  | Meaning       | Example                   |
| -------- | ------------- | ------------------------- |
| `SELECT` | Retrieve data | `SELECT * FROM students;` |

---

### 4) TCL — Transaction Control Language
- tRANSACTION: pACKAGE OF SQL STATEMENT
- Savepoints and control changes
  
| Command             | Meaning                        | Example                |
| ------------------- | ------------------------------ | ---------------------- |
| `START TRANSACTION`    | Begin transaction block   | `START TRANSACTION`      |
| `COMMIT`            | Save all changes permanently   | `COMMIT;`              |
| `ROLLBACK`          | Undo changes since last commit | `ROLLBACK;`            |
| `SAVEPOINT`         | Set a point to rollback to     | `SAVEPOINT A;`         |
| `RELEASE SAVEPOINT` | Remove a savepoint             | `RELEASE SAVEPOINT A;` |

### ACID Properties:
1. A -> Atomicity -> transaction happens completely yes or completely not
2. C -> Consistency -> data must remain valid before and after transaction
3. I -> Isolation -> Each transaction runs independently without affect others
5. D -> Durability -> Once commited, data is saved permently even after a crash

---

### 5) DCL : Data Control Language

- Permissions & Security
- Controls who can do what

| Command  | Meaning          | Example                                 |
| -------- | ---------------- | --------------------------------------- |
| `GRANT`  | Give user access | `GRANT SELECT ON students TO user1;`    |
| `REVOKE` | Remove access    | `REVOKE SELECT ON students FROM user1;` |

**🎯 Interview Quick Notes**

- DDL changes structure, DML changes data.
- DML and TCL work together → because data changes can be rolled back.
- SELECT is DQL — many confuse it as DML.
- TRUNCATE vs DELETE:
     - TRUNCATE removes all rows quickly, can’t rollback (DDL).
     - DELETE removes specific rows, can rollback (DML).

**Q. Difference Between DDL and DML**

| Feature                | **DDL (Data Definition Language)**                                           | **DML (Data Manipulation Language)**              |
| ---------------------- | ---------------------------------------------------------------------------- | ------------------------------------------------- |
| **Purpose**            | Defines or modifies **structure** of database objects (tables, schema, etc.) | Manages or manipulates **data inside** the tables |
| **Examples**           | `CREATE`, `ALTER`, `DROP`, `TRUNCATE`, `RENAME`                              | `SELECT`, `INSERT`, `UPDATE`, `DELETE`            |
| **Affects**            | Changes the **table design** or schema                                       | Changes **table content (rows)**                  |
| **Auto Commit**        | ✅ Yes — changes are permanent automatically                                  | ❌ No — requires `COMMIT` or `ROLLBACK`            |
| **Rollback Possible?** | ❌ Cannot rollback                                                            | ✅ Can rollback before commit                      |
| **Executed by**        | Database administrator (DBA) or developer                                    | User or application program                       |

**Q. Difference between DROP, TRUNCATE, and DELETE**

| Command      | Type | What it does                                    | Rollback?             | 
| ------------ | ---- | ----------------------------------------------- | --------------------- | 
| **DROP**     | DDL  | Deletes **table structure + data** completely   | ❌ No                  |           
| **TRUNCATE** | DDL  | Deletes **all rows only** (keeps structure)     | ❌ No                  | 
| **DELETE**   | DML  | Deletes **specific rows** (or all, if no WHERE) | ✅ Yes (before commit) | 

**Example:**
| Command                            | Result                         |
| ---------------------------------- | ------------------------------ |
| `DELETE FROM students WHERE id=3;` | Removes only 1 row (id=3)      |
| `TRUNCATE TABLE students;`         | Removes all rows (table empty) |
| `DROP TABLE students;`             | Removes table completely       |

| ❓ Question                                       | 💡 Smart Answer                                                  |
| ------------------------------------------------ | ---------------------------------------------------------------- |
| **Can we rollback TRUNCATE?**                    | No, it’s a DDL command → auto commits.                           |
| **Is DELETE faster than TRUNCATE?**              | No, TRUNCATE is faster because it doesn’t log each row deletion. |
| **What happens to table structure after DROP?**  | It’s removed completely — can’t access or insert data again.     |
| **Is TRUNCATE same as DELETE without WHERE?**    | No — TRUNCATE resets identity counters & can’t be rolled back.   |
| **Which command resets AUTO_INCREMENT counter?** | TRUNCATE (DROP + CREATE internally).                             |
| **Can DELETE activate triggers?**                | Yes, DELETE fires triggers. TRUNCATE doesn’t.                    |


---
 
## Datatypes in SQL:

- Data types **define the type of data** a column can store in a table.
- They decide how much memory is used and what kind of operations are allowed on that column.

```
CREATE TABLE Students (
  id INT,           -- stores whole numbers
  name VARCHAR(50), -- stores text
  marks FLOAT,      -- stores decimals
  dob DATE          -- stores dates
);

```

| Category              | Example types               | Used for                       |
| --------------------- | --------------------------- | ------------------------------ |
| 1. Numeric            | INT, DECIMAL, FLOAT, DOUBLE | Numbers                        |
| 2. String / Character | CHAR, VARCHAR, TEXT         | Text / Characters              |
| 3. Date & Time        | DATE, DATETIME, TIME, YEAR  | Dates / Times                  |
| 4. Others (Special)   | BOOLEAN, ENUM, SET, JSON    | True/False, Options, JSON data |

---

### NUmeric Datatypes

| Type              | Range (Signed)          | Bytes | Example                       |
| ----------------- | ----------------------- | ----- | ----------------------------- |
| **TINYINT**       | -128 to 127             | 1     | small flags (like true/false) |
| **SMALLINT**      | -32,768 to 32,767       | 2     | small numbers                 |
| **MEDIUMINT**     | -8 million to 8 million | 3     | moderate                      |
| **INT / INTEGER** | -2 billion to 2 billion | 4     | most used                     |
| **BIGINT**        | very large numbers      | 8     | IDs, phone numbers            |
| ----------------- | -------------------------- | --------------------- |
| **DECIMAL(p, s)** | Fixed-point (exact)        | DECIMAL(5,2) → 999.99 |
| **FLOAT**         | Approximate (less precise) | FLOAT(7,4) → 123.4567 |
| **DOUBLE**        | Larger approximate         | DOUBLE(15,10)         |


- Use smallest numeric type that fits your data → saves storage and speeds up queries.
- Rule of thumb:
   - Use DECIMAL for money, percentages (needs accuracy).
   - Use FLOAT/DOUBLE for scientific values (speed > accuracy).
```
CREATE TABLE Marks (
  id INT PRIMARY KEY,
  total_marks INT,
  rank SMALLINT,
  salary DECIMAL,
  speed DOUBLE;
);
```

### String Character Data Types

| Type           | Description               | Max Size         | Example                   |
| -------------- | ------------------------- | ---------------- | ------------------------- |
| **CHAR(n)**    | Fixed-length string       | up to 255        | ‘INDIA’, ‘USA’            |
| **VARCHAR(n)** | Variable-length string    | up to 65,535     | ‘Mumbai’                  |
| **TEXT**       | Large text                | up to 65,535     | article body              |
| **MEDIUMTEXT** | Bigger                    | up to 16 million |                           |
| **LONGTEXT**   | Very large                | up to 4GB        | long descriptions         |
| **ENUM**       | One value from a list     | predefined       | ENUM('Male','Female')     |
| **SET**        | Multiple values from list | predefined       | SET('Java','SQL','React') |

```
CREATE TABLE Employee (
  emp_id INT,
  emp_name VARCHAR(50),
  gender ENUM('Male','Female','Other'),
  skills SET('Java','SQL','Python','HTML')
);
```


#### CHAR vs VARCHAR difference (important interview Q):

| CHAR                                      | VARCHAR                      |
| ----------------------------------------- | ---------------------------- |
| Fixed length                              | Variable length              |
| Faster, uses extra space                  | Saves space, slightly slower |
| Use for fixed-size data (e.g., PIN, code) | Use for names, addresses     |

---

### Date and Time Data Types

| Type          | Format                          | Example               |
| ------------- | ------------------------------- | --------------------- |
| **DATE**      | YYYY-MM-DD                      | ‘2025-11-12’          |
| **DATETIME**  | YYYY-MM-DD HH:MM:SS             | ‘2025-11-12 13:30:00’ |
| **TIMESTAMP** | same as DATETIME (auto-updates) | ‘2025-11-12 13:30:00’ |
| **TIME**      | HH:MM:SS                        | ‘13:30:00’            |
| **YEAR**      | YYYY                            |  2025                 |

```
CREATE TABLE Orders (
  order_id INT,
  order_date DATE,
  order_time TIME,
  joiningYear YEAR, 
  created_at TIMESTAMP 
);
```

#### Remember:
- Use DATETIME for manual control.
- Use TIMESTAMP when you want auto record of insert/update time.

---

### Boolean and Other Special Data Types

| Type                | Description                 | Example             |
| ------------------- | --------------------------- | ------------------- |
| **BOOLEAN / BOOL**  | True (1) or False (0)       | `is_active BOOLEAN` |
| **JSON**            | Stores structured JSON data | `details JSON`      |
| **BLOB / LONGBLOB** | Binary data (images/files)  | `profile_pic BLOB`  |

```
CREATE TABLE Settings (
  id INT,
  is_active BOOLEAN,
  preferences JSON
);

```

## ALL MAJOR DATATYPES:

```
CREATE TABLE Students (
  student_id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(100),
  gender ENUM('Male','Female','Other'),
  dob DATE,
  marks DECIMAL(5,2),
  passed BOOLEAN,
  admission_time DATETIME,
  address TEXT
);
```

### Interview Questions

| Question                                                  | Answer (Short & Rememberable)                                                    |
| --------------------------------------------------------- | -------------------------------------------------------------------------------- |
| **Q1:** Difference between CHAR and VARCHAR?              | CHAR = fixed length; VARCHAR = variable length.                                  |
| **Q2:** When to use DECIMAL instead of FLOAT?             | When you need **exact precision**, like money.                                   |
| **Q3:** What is ENUM and SET in MySQL?                    | ENUM → one option; SET → multiple options from predefined list.                  |
| **Q4:** Difference between DATE, DATETIME, and TIMESTAMP? | DATE → only date, DATETIME → full date+time, TIMESTAMP → date+time auto updates. |
| **Q5:** What is the use of JSON type?                     | To store structured JSON data inside a single column (like nested info).         |
| **Q6:** Why use the right data type?                      | To save memory, improve performance, and ensure data validity.                   |

---


## Constraints: 

- Constraints are rules applied to table columns to restrict invalid data, ensure uniqueness, and maintain relationship integrity.
- Constraints are applied while creating or altering a table.

| Constraint      | Meaning                                   | Example / Notes                                                    |
| --------------- | ----------------------------------------- | ------------------------------------------------------------------ |
| **PRIMARY KEY** | UNIQUE + NOT NULL (identifies each row)             | `id INT PRIMARY KEY`                                               |
| **FOREIGN KEY** | Links two tables (maintains relationships)     | `student_id INT, FOREIGN KEY (student_id) REFERENCES Students(id)` |
| **NOT NULL**    | Column cannot have Empty/NULL values  | `name VARCHAR(50) NOT NULL`                                        |
| **UNIQUE**      |  No duplicate values allowed      | `email VARCHAR(100) UNIQUE`                                        |
| **CHECK**       | Restricts data using a satisfying condition   | `age INT CHECK (age >= 18)`                                        |
| **DEFAULT**     | Sets a default value when no value is provided    | `status VARCHAR(10) DEFAULT 'Active'`                              |

---

### Primary Key:
- A primary key in SQL is a column in a database table that uniquely identifies each row within that table
- Cannot be NULL
- Only one PK per table

```
CREATE TABLE Students (
  id INT PRIMARY KEY
);

```
- Each student must have a unique id which is NOT NULL
- Primary Key cannot:
   - be NULL
   - be duplicate value,
   - be changed easily (used for identification)

**Interview Question:**
**Q: Can a table have more than one primary key?**
A: No, but it can have composite primary key (multiple columns together).

**Q: Difference between PRIMARY KEY and UNIQUE?**
A: PK → Cannot be NULL, only one per table; UNIQUE → Can be NULL, multiple per table.

### Foreign Key:
- A foreign key in a database is a relationship/link between two tables. It ensures that a field (or group of fields) in one table matches a primary key in another table.
- Primary key of one table is foreign key of another table
- to delete one row from other table which has relationship of PK and FK use ON DELETE - CASCADE and SET NULL

**STudent table**
| Student_ID | name    | Year                                         |
| ----------- | ------- | --------------------------------------------- |
| 1           | Alice   |  2   |
| 2           | Bob     |   3      |
| 3           | Charlie | 1 |

- year is primary key

**Year table**
| Year | Room    | Block                                         |
| ----------- | ------- | --------------------------------------------- |
| 1           | 501   |  2   |
| 2           | 601     |   3      |
| 3           | 701 | 1 |

- year is foregin key of student table

# PENDING NOTES FOR OTHER CONSTRAINTS

---

**Example: Table Students With all Constarints:**

```
CREATE TABLE students (
    roll_no INT PRIMARY KEY,
    name VARCHAR(50) NOT NULL,
    age INT CHECK(age >= 5),
    email VARCHAR(50) UNIQUE,
    city VARCHAR(20) DEFAULT 'Mumbai'
);
```

* Multiple column creation (Composite)

```
CREATE TABLE person (
  first_name varchar(50) NOT NULL,
  last_name  varchar(50) NOT NULL,
  age        int,
  CONSTRAINT UC_person Primary Key (age, first_name)
);

```

- Drop
```
ALTER TABLE person
DROP INDEX UC_person;
```
---

## Operators in SQL

- Operators are symbols or keywords **used to perform operations on data**
- like comparing, adding, filtering, or combining results.
- They’re used inside SQL statements, **mainly in WHERE and HAVING clauses.**
  
| Category   | Keywords                   |  Use                                 |
| ---------- | -------------------------- | ------------------------------------ |
| Arithmetic | +, -, *, /, %              |  Math operations ->	`salary + bonus` |
| Comparison | =, !=, >, <, >=, <=        |  Compare values ->	`salary > 50000`
| Logical    | AND, OR, NOT               |  Combine multiple conditions	-> `age > 20 AND city = 'Delhi'` | 
| Special    | IN, BETWEEN, LIKE, IS NULL |  Match patterns, check nulls, etc. ->	`LIKE, IN, BETWEEN, IS NULL` | 
| Set        | UNION, INTERSECT, EXCEPT   |  Combine multiple queries-> `UNION, INTERSECT, EXCEPT  |

### 1) Arithmetic

| Operator | Meaning             | Example            |
| -------- | ------------------- | ------------------ |
| `+`      | Addition            | `salary + bonus`   |
| `-`      | Subtraction         | `price - discount` |
| `*`      | Multiplication      | `quantity * rate`  |
| `/`      | Division            | `total / 2`        |
| `%`      | Modulus (remainder) | `marks % 2`        |

```
SELECT emp_name, salary + bonus AS total_income
FROM employees;
```
- Adds both salary and bonus to give the total income of the employee;

### 2) Relational

- Used to compare two values — returns TRUE or FALSE.

| Operator     | Meaning               | Example           |
| ------------ | --------------------- | ----------------- |
| `=`          | Equal to              | `city = 'Mumbai'` |
| `!=` or `<>` | Not equal to          | `dept <> 'HR'`    |
| `>`          | Greater than          | `salary > 50000`  |
| `<`          | Less than             | `age < 30`        |
| `>=`         | Greater than or equal | `marks >= 40`     |
| `<=`         | Less than or equal    | `marks <= 90`     |

```
SELECT * FROM employees WHERE salary >= 50000;
```
- retrieves employees' data with more than or equal to salary 50000;

### 3) Logical Operators

- Used to combine multiple conditions.

| Operator | Meaning                     | Example                           |
| -------- | --------------------------- | --------------------------------- |
| `AND`    | All conditions must be true | `salary > 50000 AND dept = 'IT'`  |
| `OR`     | At least one condition true | `city = 'Pune' OR city = 'Delhi'` |
| `NOT`    | Negates condition           | `NOT dept = 'HR'`                 |

```
SELECT * FROM employees
WHERE (dept = 'HR' OR dept = 'IT') AND salary > 40000;
```
- Retrieves data where department is either HR or IT and salary more than 40k;

### 4) Special Operators
- used for pattern matching, checking ranges, nulls, and lists.

| Operator                  | Meaning                                                 |  Example                 |
| ------------------------- | ------------------------------------------------------- | ------------------------- |
| **BETWEEN**               | Checks if value lies **between two values**             | `marks BETWEEN 70 AND 90`         |
| **IN**                    | Checks if value matches **any value from a list**       | `city IN ('Delhi', 'Mumbai', 'Pune')`         |
| **LIKE**                  | Used for **pattern matching** with wildcards            | `name LIKE 'A%'`    |
| **IS NULL / IS NOT NULL** | Checks for **NULL values**                              |  `bonus IS NULL`     |
| **ANY / SOME**            | Compares value with **any value in subquery**           | `salary > ANY (SubQuery)`      |
| **ALL**                   | Compares value with **all values in subquery**          |  `salary > ALL (SubQuery)`         |
| **EXISTS**                | Checks if **subquery returns rows**                     | `EXISTS (SubQuery)`  |


```
SELECT * FROM employees 
WHERE salary BETWEEN 20000 AND 40000;
```
- Returns all employees whose salary is ≥ 20000 and ≤ 40000

```
SELECT * FROM students 
WHERE city IN ('Mumbai', 'Delhi', 'Pune');
```
- Returns students who live in Mumbai, Delhi, or Pune
- Instead of using city = 'Mumbai' **OR** city = 'Delhi' **OR** city = 'Pune', just use **IN**

```
SELECT * FROM employees 
WHERE name LIKE 'S%';
```
- Finds names starting with S

**WildCards for Like**

| Symbol           | Meaning                      | Example                                 |
| ---------------- | ---------------------------- | --------------------------------------- |
| `%`              | Any number of characters     | `'A%'` → Starts with A                  |
| `_`              | Exactly one character        | `'A_'` → 2-letter names starting with A |
| `[ ]`            | Any one of characters inside | `'[ST]%'` → Starts with S or T          |
| `[^ ]` or `[! ]` | Not these characters         | `'[^A]%'` → Doesn’t start with A        |


```
SELECT * FROM orders 
WHERE delivery_date IS NULL;
```
- Finds records where delivery date is not filled.
- `=` doesn’t work with NULL → must use `IS NULL`.
- NULL = missing or undefined value (not zero or empty).

```
SELECT * FROM employees 
WHERE salary > ANY (SELECT salary FROM interns);
```
- Returns employees whose salary is greater than any intern’s salary
- `ANY` and `SOME` mean the same thing.

```
SELECT * FROM employees 
WHERE salary > ALL (SELECT salary FROM interns);
```
- Returns employees whose salary is greater than all intern salaries
- “ALL” means strongest condition must beat every value.

**Interview Questions:**
| Question                              | Answer                                                                                            |
| ------------------------------------- | ------------------------------------------------------------------------------------------------- |
| **BETWEEN inclusive or exclusive?**   | Inclusive — includes both lower and upper limits                                                  |
| **Difference between IN and EXISTS?** | `IN` compares values; `EXISTS` checks if rows exist                                               |
| **Difference between ANY and ALL?**   | `ANY` = true if condition is true for **any one value**; `ALL` = must be true for **every value** |
| **Can we use LIKE with numbers?**     | No, only with text (CHAR, VARCHAR)                                                                |
| **Why IS NULL instead of = NULL?**    | Because NULL is not a value; it represents “unknown”                                              |


### 5) Set Operators
- Set operators are used to combine the results of two or more SELECT queries into a single result set.
- Used to combine results of multiple SELECT queries.

| Operator           | Meaning                                | Example                                                |
| ------------------ | -------------------------------------- | ------------------------------------------------------ |
| `UNION`            | Combines results of two queries, removes duplicates   | `SELECT city FROM cust1 UNION SELECT city FROM cust2;` |
| `UNION ALL`        | Combines results of two queries, keeps duplicates     | same as above                                          |
| `INTERSECT`        | Returns common rows between two Select queries    | (not in MySQL, but exists in others)                   |
| `EXCEPT` / `MINUS` | Returns rows from first query not in second | (not in MySQL, exists in SQL Server/Oracle)            |

**Example:**

**Table 1: Sep_Batch**

| name  |
| ----- |
| Mastan  |
| Dhanraj |
| Krupa |
| Safiya |
| Haripawan |
| Bhavya   |


**Table 1: Aug_Batch**

| name  |
| ----- |
| Afrin |
| Ujjal   |
| Sk Naim Ali  |
| Bhavya   |

```
SELECT name FROM  Sep_Batch
UNION
SELECT name FROM Aug_Batch;
```

**Output:**

| name  |
| ----- |
| Mastan  |
| Dhanraj |
| Krupa |
| Safiya |
| Haripawan |
| Afrin |
| Ujjal   |
| Sk Naim Ali  |
| Bhavya   |

- `Union` removes duplicate Bhavya record
- If we do `UNION ALL` then it will include duplicate Bhavya as well

```
SELECT name FROM  Sep_Batch
INTERSECT
SELECT name FROM Aug_Batch;
```
**Output:**

| name  |
| ----- |
| Bhavya |

- INTERSECT gives the Common between both.
- (Note: MySQL doesn’t directly support `INTERSECT`; use `INNER JOIN` instead)

```
SELECT name FROM batch_2024
MINUS/EXCEPT
SELECT name FROM batch_2025;
```
**Output**

| name  |
| ----- |
| Mastan  |
| Dhanraj |
| Krupa |
| Safiya |
| Haripawan |

- Minus Bhavya

**Interview Example Question**
**Q: Difference between UNION and JOIN?**
- UNION combines the result of two `SELECT` queries vertically (row-wise), while `JOIN` combines horizontally (column-wise) based on a condition.
- JOINS Requires a relation (usually a foreign key). SETs work on the results of independent queries.

---

## Clauses in SQL

- A clause is a part of a SQL query that performs a specific task, such as filtering, sorting, grouping, or limiting data.
- Think of a clause like a sentence part:
1. SELECT → choose columns
2. WHERE → apply conditions
3. GROUP BY → group rows
4. HAVING → apply conditions on grouped data
5. ORDER BY → sort results
6. LIMIT → limit number of rows

---

### 1) WHERE Clause
- Used to filter rows based on a condition.
- Works with `SELECT, UPDATE, and DELETE.`

**Syntax:**
```
SELECT * FROM table_name WHERE condition;
```

**Example:**
```
SELECT * FROM students WHERE city = 'Pune';
```
- Returns only rows where city = Pune.

- Operators you can use:
- `=, !=, >, <, >=, <=`
- `BETWEEN, IN, LIKE, IS NULL, AND, OR, NOT`

**Example:**
```
SELECT * FROM students WHERE age BETWEEN 18 AND 25;
SELECT * FROM students WHERE name LIKE 'N%';
SELECT * FROM students WHERE city IN ('Pune', 'Mumbai');
```

**Interview Tip:**
- WHERE filters before grouping, HAVING filters after grouping.

---

### 2) ORDER BY Clause
- Used to sort results in ascending or descending order.

**Syntax:**
```
SELECT * FROM students ORDER BY age ASC;
SELECT * FROM students ORDER BY age DESC;
```

- You can sort by multiple columns:
```
SELECT * FROM students ORDER BY city ASC, age DESC;
```

**Interview Tip:**
- ASC = ascending (default)
- DESC = descending
- Works even on computed columns (like ORDER BY age + 2)

---

### 3) GROUP BY Clause

- Used to group rows having the same values in one or more columns, often used with aggregate functions `(SUM, AVG, COUNT, MAX, MIN).`

**Example:**
```
SELECT city, COUNT(*) AS total_students
FROM students
GROUP BY city;
```

| city   | total_students |
| ------ | -------------- |
| Pune   | 3              |
| Mumbai | 2              |
| Delhi  | 1              |

**Interview Tip:**
- All non-aggregated columns in SELECT must be in GROUP BY.

**Good:**
```
SELECT city, COUNT(*) FROM students GROUP BY city;
```

**Wrong:**
```
SELECT name, COUNT(*) FROM students GROUP BY city;
```

---

### 4) HAVING Clause

- Used to filter grouped results (unlike WHERE, which filters rows before grouping).

**Example:**
```
SELECT city, COUNT(*) AS total
FROM students
GROUP BY city
HAVING COUNT(*) > 1;
```
- Shows only cities with more than 1 student.

**Interview Tip:**
- WHERE → before GROUP BY
- HAVING → after GROUP BY
**“Where first, Having after”**

---

### 5) LIMIT Clause (MySQL specific)

- Used to limit the number of rows returned.

**Syntax:**
```
SELECT * FROM students LIMIT 3;
```

**Example:**
```
SELECT * FROM students ORDER BY age DESC LIMIT 2;
```

- Returns top 2 oldest students.

**Interview Tip:**
- In SQL Server, TOP is used instead of LIMIT.
- In Oracle, use ROWNUM.

---

### 6) DISTINCT Keyword

- Removes duplicate values from the result set.

**Example**
```
SELECT DISTINCT city FROM students;
```

- If you have duplicate city names, only unique ones will appear.

**Interview Tip:**

- DISTINCT applies to the whole selected combination of columns.

**Example:**

- SELECT DISTINCT name, city FROM students;
→ returns unique (name, city) pairs.

---

## Interview QUestion on Clauses:

| Question                                             | Answer                                                                                                         |
| ---------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| 1️ Difference between WHERE and HAVING?             | WHERE filters before grouping, HAVING filters after grouping (on aggregated data).                             |
| 2️ Can you use WHERE with GROUP BY?                 | Yes, WHERE filters rows before grouping happens.                                                               |
| 3️ Can you use both WHERE and HAVING in same query? | Yes. Example:<br>`SELECT city, COUNT(*) FROM students WHERE age>18 GROUP BY city HAVING COUNT(*)>2;`           |
| 4️ Difference between ORDER BY and GROUP BY?        | ORDER BY sorts rows in asc, desc order; GROUP BY combines similar rows.                                                           |
| 5️ What is the use of LIMIT?                        | Restrict number of rows returned — mainly used for pagination or performance.                                  |
| 6️ Can we use column alias in ORDER BY?             | Yes, e.g. `SELECT age AS a FROM students ORDER BY a DESC;`                                                     |
| 7️ Can HAVING work without GROUP BY?                | Yes, technically possible — acts like WHERE for aggregates: `SELECT COUNT(*) FROM students HAVING COUNT(*)>5;` |
| 8️ Difference between DISTINCT and GROUP BY?        | Both remove duplicates, but GROUP BY can use aggregate functions, DISTINCT cannot.                             |
| 9️ What is the order of SQL execution?              | FROM → WHERE → GROUP BY → HAVING → SELECT → ORDER BY → LIMIT                                                   |
| 10 Can ORDER BY come before WHERE?                   | No, ORDER BY must always be last (before LIMIT).                                                               |
| 11 How do you remove duplicates from a result? | Using DISTINCT `SELECT DISTINCT city FROM customers;` |
| 12 What does LIKE ‘%a%’ mean? | It finds values that contain the letter ‘a’ anywhere in them. 'A%' → starts with A, '%A' → ends with A, '%A%' → contains A anywhere |

---

### SUMMARY CHEATSHEET for Clauses 

| Clause                    | Meaning                                          | Example                                                                   | Output Purpose                                 |
| ------------------------- | ------------------------------------------------ | ------------------------------------------------------------------------- | ---------------------------------------------- |
| **WHERE**                 | Filters rows based on condition                  | `SELECT * FROM employees WHERE salary > 50000;`                           | Shows only employees earning > 50K             |
| **ORDER BY**              | Sorts data in ascending/descending order         | `SELECT * FROM students ORDER BY marks DESC;`                             | Sorts students by marks (highest first)        |
| **GROUP BY**              | Groups rows based on common values               | `SELECT dept, COUNT(*) FROM employees GROUP BY dept;`                     | Groups employees by department                 |
| **HAVING**                | Applies condition **on groups** (after GROUP BY) | `SELECT dept, COUNT(*) FROM employees GROUP BY dept HAVING COUNT(*) > 5;` | Shows departments having more than 5 employees |
| **LIMIT** *(MySQL only)*  | Restricts number of rows displayed               | `SELECT * FROM orders LIMIT 10;`                                          | Shows only first 10 rows                       |
| **DISTINCT**              | Removes duplicate rows                           | `SELECT DISTINCT dept FROM employees;`                                    | Lists unique departments                       |
| **BETWEEN**               | Filters values in a range                        | `SELECT * FROM students WHERE marks BETWEEN 70 AND 90;`                   | Students with marks 70–90                      |
| **IN**                    | Matches multiple possible values                 | `SELECT * FROM employees WHERE dept IN ('HR', 'IT');`                     | Shows employees from HR or IT                  |
| **LIKE**                  | Pattern matching with wildcards                  | `SELECT * FROM customers WHERE name LIKE 'A%';`                           | Names starting with ‘A’                        |
| **IS NULL / IS NOT NULL** | Checks for null values                           | `SELECT * FROM orders WHERE discount IS NULL;`                            | Finds orders without discounts                 |

---

## Execution flow of SQL Commands:

| Step             | Clause                              | Description                |
| ---------------- | ----------------------------------- | -------------------------- |
| **1️⃣ FROM**     | Selects table(s) to fetch data from | `FROM employees`           |
| **2️⃣ JOIN**    | JOINS Before filtering              | `JOIN classes ON e.emp_id = d.emp_id;`     |
| **2️⃣ WHERE**    | Filters rows (before grouping)      | `WHERE salary > 50000`     |
| **3️⃣ GROUP BY** | Groups rows based on column(s)      | `GROUP BY dept_id`         |
| **4️⃣ HAVING**   | Filters groups (after grouping)     | `HAVING COUNT(*) > 3`      |
| **5️⃣ SELECT**   | Chooses which columns to show       | `SELECT dept_id, COUNT(*)` |
| **6️⃣ ORDER BY** | Sorts the final result              | `ORDER BY dept_id`         |

**E,g,**
```
SELECT department, AVG(salary)
FROM employees
WHERE age > 25
GROUP BY department
HAVING AVG(salary) > 60000
ORDER BY AVG(salary) DESC;
```
#### Execution happens like this:

1. **FROM employees** → takes all data from employees table
2. **JOINS** (if)
3.** WHERE age > 25** → filters rows where age > 25
4. **GROUP BY department** → groups remaining rows department-wise
5. **HAVING AVG(salary) > 60000** → filters groups by average salary
6. **SELECT department, AVG(salary)** → selects columns to display
7. **ORDER BY AVG(salary) DESC** → sorts result by salary descending

### Interview Questions: 

| Question                                               | Ideal Answer                                                                      |
| ------------------------------------------------------ | --------------------------------------------------------------------------------- |
| **Q1. What is the order of SQL query execution?**      | FROM → WHERE → GROUP BY → HAVING → SELECT → ORDER BY                              |
| **Q2. Why does WHERE execute before SELECT?**          | Because WHERE filters data before the final columns are chosen.                   |
| **Q3. Difference between WHERE and HAVING?**           | WHERE filters **rows before grouping**, HAVING filters **groups after grouping**. |
| **Q4. Does ORDER BY execute before GROUP BY?**         | No. GROUP BY happens first, ORDER BY comes last.                                  |
| **Q5. Which clauses are mandatory in a SELECT query?** | Only SELECT and FROM are mandatory. Others are optional.                          |


