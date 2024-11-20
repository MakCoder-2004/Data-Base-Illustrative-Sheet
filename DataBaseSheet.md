# What is DataBase?

  - A database is an organized collection of data so that it can be easily accessed. Database Management Systems (DBMS) are used to manage these databases.

# Types of DBMS

  - Non-Relational (DBMS): File System, XML..etc.
  - Relational (RDBMS): An enhanced version of DBMS but with relations such as SQLServer, Oracle, MySQL ..etc.

---------------------------------------------------------------------------------

# Frequently used names In RDBMS

  - Table or Entity Set
  - Column or Field or Attribute 
  - Row or Entity or Record or Tupel

---------------------------------------------------------------------------------

**NULL**      "NULL is not the same as a blank space or a zero"
--
  - "NULL" is a special marker used to indicate that a data value does not exist in the database. 
  - It represents a missing or unknown value in a table column.

---------------------------------------------------------------------------------

**Primary Key**
--
  - A primary key is a column or set of columns that uniquely identifies each row or record in the table.
  - Each table in a relational database must have a primary key, and it should be a non-null value.
  - It is most likely to be numerical instead of String for easy access and for fast accessing.
  - Each Table must have a Primary Key.

**Foreign Key**
--
  - A foreign key is a column or set of columns in a table that refers to the primary key of another table. 
  - It is the relationship between two tables, allowing data to be shared and linked between them. 
  - Ensures that any value in the foreign key column must exist in the primary key column of the related table.

**Primary VS Foreign Keys**
--
  - A primary key uniquely identifies a record in a table, while a foreign key establishes a relationship between two tables by referencing the primary key of another table.

---------------------------------------------------------------------------------

# Redundancy (Data Duplication): **"Not Always BAD, sometimes can be useful"**
  
  **Problems?**
  - Wasting space
  - Data Inconsistency
  - Data Corruption
  - Integrity Problem
  - Hard to maintain

  **Solutions?**
  - Normalization Techniques -> Organizing and separating Data into multiple Tables.
  - Relational Tables (Using Primary and Foreign Keys).
  - Putting Constraints (شروط) on the data.

---------------------------------------------------------------------------------

# Data Integrity

  - It refers to the accuracy, consistency, and reliability of the data.

  - **Effectiveness** is doing the right things to obtain high-quality results.
  - **Efficiency** is doing things in the right way in the least amount of time with the least amount of resources.
  - **Productivity** = Effectiveness + Efficiency

  **Problems (factors that can impact data integrity)?**
  - Data corruptions
  - Hardware or Software failure.
  - Data Transfer Errors.

  **Solutions?**
  - Establishing appropriate policies and procedures.
  - Implement appropriate Technologies such as encryption, backups, and access controls.
  - To maintain data integrity we use Constraints.

  **Types of data integrity:**
  1. Entity integrity -> This ensures that each row or record in a table is unique and can be uniquely identified.
  2. Referential integrity -> This ensures that relationships between tables are maintained.
  3. Domain integrity -> This ensures that data is within acceptable ranges.
  4. Business integrity -> This ensures that data meets business rules and requirements. 

  What are atomic values?
  - Atomic values are the smallest possible units of data that can be stored in a database.
  - They cannot be further divided or decomposed into smaller parts.
  - Atomic values are also known as single-valued or indivisible attributes.
    
  **Why use atomic values?**
  - Using atomic values in your database schema can help you achieve data integrity and normalization.

---------------------------------------------------------------------------------
# Database Design

## Hierarchical Model

- The database records are arranged as a tree with roots and several branches/children.
-  Records are dependent and arranged in multilevel structures, consisting of one root record **(Primary Key)** and any number of subordinate levels.
  
### Advantages:-
1. Conceptual simplicity
2. Centralization of data
3. Data Integrity
4. Data independence
5. Efficiency

### Disadvantages:-
1. Limited representation of data relationships => Don't allow Many to Many
2. Complex implementation
3. Structural Dependence => Programs are affected by changes in the file structure
4. Lack of Standards
---------------------------------------------------------------------------------

## Network Model

- Records linked by pointers

### Advantages:-
1. Conceptual simplicity
2. Handles more relationship types
3. Data access flexibility
4. Data integrity
5. Conformance to standards

### Disadvantages:-
1. System complexity
2. Structural dependence -> Programs are affected by changes in the file structure
   
---------------------------------------------------------------------------------
## ERD (Entity Relationship Diagram)

**ER Diagram in RDBMS:**
- Structural design of the database. You can use an online ERD maker like (drawsql.app).

- **Based on:**
  - Entities
  - Relationships
  - Attributes

- The cost of updating an ERD is much cheaper than updating the database after it's built.

- ERD helps both users and database developers preview the structure of the database before implementation.

### Advantages:-
1. Easier database design, implementation, management and use
2. Flexibility to change data structures
3. Structured Query Language (SQL) => allows the user to specify what must be done without specifying how it must be done.
4. Providing backup and recovery services
   
### Disadvantages:-
1. Hides the implementation complexities and the physical data storage details from the users

### Steps to Create ERD:
1. Entity Identification
2. Relationship Identification
3. Cardinality Identification
4. Attributes Identification
5. Create ERD


### Entity
- **Rectangle shape**
  - **Strong Entity:** Has a Primary Key, represented by a single rectangle.
  - **Weak Entity:** It doesn't have a primary key, which is represented by a double rectangle.
  - **Associative Entity:** Models a many-to-many relationship between two other entities.
  - **Aggregation Entity:** Represents the relation between two entities treated as a single entity.
  

### Relationships
- **Rhombus + Lines linking between two entities**
  - We can have more than one relationship between two entities.
#### Types of Relationships
- **Recursive Relationship**(Unary Relationship): Participates more than once in a relationship type with different roles.
- **One-to-One Relationship:** When a single element of an entity is associated with a single element of another entity.
  - **Example:** "is-a" or "has-a" or "set".
- **One-to-Many Relationship:** When a single element of an entity is associated with more than one element of another entity.
  - **Example:** Many customers placed many orders.
- **Many-to-One Relationship:** When more than one element of an entity is associated with a single element of another entity.
  - **Example:** One order is placed by many customers.
- **Many-to-Many Relationship:** When more than one element of an entity is associated with more than one element of another entity.
  - **Example:** Many students enroll in many courses.

#### Cardinality vs. Ordinality Relationship
- **Represented in brackets (.. , ..) -> (ordinality, cardinality)**
  - **Cardinality:** Refers to the maximum number of times an instance in one entity can relate to instances of another entity.
  - **Ordinality:** Refers to the minimum number of times an instance in one entity can relate to instances of another entity.

#### Crow's Foot Notation Symbols
- **0|** -> one or zero
- **||** -> one and only one
- **0<** -> zero or many
- **|<** -> one or many
  

### Attributes
- **Ellipse shape**
- **Elements (information) of the entities**
- Represents some property of interest that describes an entity, such as the employee’s name or salary.
  
#### Types of Attributes
1. **Key Attribute:** If an element is underlined, it is the Primary Key.
2. **Composite Attribute:** An element composed of many attributes.
3. **Multivalued Attribute:** An element that can store many values (e.g., phone 1, phone 2).
4. **Derived Attribute:** An element derived from another attribute.

---------------------------------------------------------------------------------

# Relational Schema

- Relation schema defines the design and structure of the relation as it consists of the relation name.
- relational databases it is divided into database tables.
- It is a set of relational tables and associated items that are related to one another.
- It is a set of (attributes/field names/column names) and every attribute would have an associated domain.

**Conversions**
---------------

- "Self Referential ---> Relational Schema"
  - For ex; Many Employees can manage many other Employees, so we link the ID of the manager with the ID of the employee he manages.

- "Composite-Multivalued-Derived Attributes ---> Relational Schema"
  - We only take the roots of any composite attribute.
  - We don't take the derived attributes.
  - We don't take multiple valued attributes but we make another table for this attribute and link it with the entity, ex; multiple phone numbers for many users.

- "One-to-One ---> Relational Schema"
  - We link an entity's Foreign key with another entity's Primary key.
  - The Primary key of an entity is also the foreign key in another entity that are linked together.
  - For ex; the card ID is the Primary key in the AccessCard Table and Foreign for the Employees Table.

- "One-to-Many/Many-to-One ---> Relational Schema"
  - We put the primary key from the 'one' side entity to the 'many' side entity as a foreign key.

- "Many-to-Many ==> Relational Schema"
  - We make a Bridge Table for many-to-many relationships.
  - We put the primary key of the two entities linked to it in the bridge table.

- "Generalization and Specialization to Relational Schema"
  - Take the primary key from the parent entity and put it as a foreign key in the child entity.

### Three-schema architecture
1. Insulation of programs and data.
2. Support of multiple user views.
3. Store the database description.

- **External Schema** is the part of the database that a particular user group is interested in and hides the rest of the database from that user group.
- **Conceptual Schema** specifies the entities, the attributes of the entities, the relationships among the entities, and constraints on the entities.
  
---------------------------------------------------------------------------------

# Generalization

**Generalization is a BOTTOM-UP approach.**

It is the process of extracting common properties from a set of entities and creating a generalized entity from them.

## Example

- **Student Entity** has (Name, Age, Roll_no) with common attributes.
  - Generalized Entity with those common attributes.

- **Employee Entity** has (Name, Age, Birth_date) attributes.
  - Generalized Entity with those common attributes.

## How to Link Entities to the General Entity?

- A symbol of a 'triangle' linking the two entities with specific/common attributes (uses/has) to the General Entity.

---------------------------------------------------------------------------------

# Specialization  **"Specialization is Bottom-Up approach."**

- It is a higher-level entity divided into multiple specialized lower-level entities.

## Example

- Employee entity has many specializations like (Professor, Developer, Secretary)
  - so there are many specializations from the person Entity

- How to link The Specialized Entities to the Main Entity?
  - A symbol of an "Upside down Triangle" linking between the main and the specialized entities with specific relationship.

---------------------------------------------------------------------------------

# SQL Server:

- **What is SQL?**
  - Structured Query Language used to communicate and access the database.
  - DMS that uses SQL: Oracle, Sybase, Microsoft SQL Server, etc...

  **Types of SQL:**
  1. **Data Definition Language (DDL)**
     - Create
     - Alert
     - Drop
     - Truncate
  2. **Data Manipulation Language (DML)**
     - Insert
     - Update
     - Delete
  3. **Data Control Language (DCL)**
     - Grant
     - Revoke
  4. **Transaction Control Language (TCL)**
     - Commit
     - Rollback
     - Save point
  5. **Data Query Language (DQL)**
     - Select

---------------------------------------------------------------------------------

**SQL Data Types:**
-----------------
  
  - int
  - decimal
  - money
  - small money

  - varchar(Max_limit)
  - nvarchar -> allows unicode

  - date
  - time
  - datetime
  - timestamp

  - image

---------------------------------------------------------------------------------

# Database Backup and Restore


**Full Backup:**
--

- Right mouse click on your database, then in tasks choose backup
or
- In Query
```sql
BACKUP DATABASE MyDatabase1
TO DISK = 'location path';
```

  -----------------------------------------------------------------

**Differential Backup:** 'save the last changes made to an existing backup'
--

- Right mouse click on your database, then in tasks choose backup, in the backup type choose Differential.
or
- In Query
```sql
BACKUP DATABASE MyDatabase1
TO DISK = 'location path'
WITH DIFFERENTIAL;
```

  -----------------------------------------------------------------

**Restore Data:**
--

- Right mouse click on your database, then in tasks choose to restore, then Database.
or
- In Query
```sql
RESTORE DATABASE MyDatabase1
FROM DISK = 'location path';
```
    
---------------------------------------------------------------------------------

# DDL (Data Definition Language)

- **Creating DataBase:**

  - Right mouse click on the DataBase then choose New Database
  or 
  - In the Query
    ```sql
    CREATE DATABASE DBName;
    ```

  - if DataBase exists we use this to avoid errors:
      ```sql
      IF NOT EXISTS(SELECT * FROM sys.databases WHERE name = 'DBName')
      BEGIN
        CREATE DATABASE DBName;
      END
      ```

  -----------------------------------------------------------------

- **Choose Database:**
  
  - In the Drop Menu choose the name of the required DataBase
  or
  - In the Query
    ```sql
    USE DBName;
    ```

  -----------------------------------------------------------------

- **Drop Database:**

  - Right Mouse click on your database from DataBase then choose Delete
  or
  - In the Query
    ```sql
    DROP DATABASE DBName;
    ```

    - if DataBase exists we use this to avoid errors:
      ```sql
      IF EXISTS(SELECT * FROM sys.databases WHERE name = 'DBName')
      BEGIN
        DROP DATABASE koko;
      END
      ```

  -----------------------------------------------------------------

- **Create Table:**
  
  - Right Mouse click on the Table File from your DataBase then choose New Table
  or
  - In the Query
    ```sql
    CREATE TABLE table_name (
      column1 datatype PRIMARY KEY,
      column2 datatype NOT NULL,
      column3 datatype NULL,
      ....
    );
    ```

  -----------------------------------------------------------------

- **Drop Table:**

  - Right Mouse click on your Table from the Table file then choose New Table
  or
  - In the Query
    ```sql
    DROP TABLE Employees;
    ```

  -----------------------------------------------------------------

- **Alter Table Statement:**
  
  - **Add Column**
    ```sql
    ALTER TABLE TableName
    ADD column5 datatype;
    ```
  
  - **Rename Column**
    ```sql
    ALTER TABLE Employees
    RENAME COLUMN column5 TO column4;
    ```
    or
    ```sql
    exec sp_rename 'table_name.old_column_name', 'new_column_name', 'COLUMN';
    ```

  - **Rename Table**
    ```sql
    ALTER TABLE OldTableName
    RENAME TO NewTableName;
    ```
    or
    ```sql
    exec sp_rename 'old_table_name', 'new_table_name';
    ```

  - **Modify Column**
    ```sql
    ALTER TABLE Employees
    ALTER COLUMN column2 VARCHAR(100) NULL;
    ```

  - **Delete Column**
    ```sql
    ALTER TABLE Employees
    DROP COLUMN column3;
    ```

  -----------------------------------------------------------------

- **Truncate:**
  - In Query
    ```sql
    TRUNCATE TABLE TableName;
    ```

---------------------------------------------------------------------------------

**Delete VS Truncate:**
----------------------

- In the delete statement we can put 'WHERE' ---> condition

- DELETE FROM statement does not reset the auto increment while the TRUNCATE reset the identity fields.

---------------------------------------------------------------------------------

# DML (Data Manipulation Language)


- **Insert:**
  - Insert one or multiple values
    ```sql
    INSERT INTO TableName       
    VALUES
      (col1Value, col2Value, col3Value, col4Value, col5Value);
    ```

  - Insert only selected fields
    ```sql
    INSERT INTO TableName (col1, col2)
    VALUES
      (col1Value, col2Value);
    ```

  - Inserting data from a table to another one
    ```sql
    INSERT INTO NewTable
    SELECT * FROM TableName
    WHERE 'condition';  -- we can put a condition or without one
    ```
  -----------------------------------------------------------------
  
- **Update:**
  - Updating an existing row in the table

    ```sql
    UPDATE TableName
    SET col2 = 'makrious', col3 = 'Hello'
    WHERE col1 = 2; -- condition
    ```
  -----------------------------------------------------------------
  
- **Delete:**
  - Deleting an existing row in the table
 
    ```sql
    DELETE FROM TableName 
    WHERE col1 = 2; -- condition
    ```

---------------------------------------------------------------------------------

# DQL (Data Query Language)


**Select:**

  - **Printing the data of a table**
    ```sql
    SELECT * FROM TableName;
    ```

  - **Printing specific columns from the table**
    ```sql
    SELECT ID, FirstName, LastName FROM TableName;
    ```
    or
    ```sql
    SELECT DISTINCT ID FROM TableName; -- It will return the rows with Distinct IDs without repetition
    ```

  - **Printing columns but with conditions**
    ```sql
    SELECT * FROM Employees
    WHERE Gender = 'F';
    ```

  - **Printing data with order**
    ```sql
    SELECT * FROM Employees 
    ORDER BY Salary DESC; -- DESC -> Descending, ASC -> Ascending
    ```

  - **Printing the top of the table**
    ```sql
    SELECT TOP 5 * FROM Employees;
    SELECT TOP 10 PERCENT * FROM Employees;
    ```

  - **Group by**
    - Take The Items that is selected in the SELECT Statement.
    - It is mostly used with the JOIN.
    ```sql
    SELECT DepartmentID, TotalCount = COUNT(MonthlySalary), 
           TotalSum = SUM(MonthlySalary),
           Average = AVG(MonthlySalary),
           MinSalary = MIN(MonthlySalary),
           MaxSalary = MAX(MonthlySalary) 
    FROM Employees
    GROUP BY DepartmentID
    ORDER BY DepartmentID;
    ```

  - **Having**    -> we use it with the 'Group by' only for making conditions
    ```sql
    SELECT DepartmentID, TotalCount = COUNT(MonthlySalary), 
           TotalSum = SUM(MonthlySalary),
           Average = AVG(MonthlySalary),
           MinSalary = MIN(MonthlySalary),
           MaxSalary = MAX(MonthlySalary) 
    FROM Employees
    GROUP BY DepartmentID
    HAVING COUNT(MonthlySalary) > 100;
    ```

  - **Concatenate multiple columns together**
    ```sql
    SELECT ID, FullName = FirstName + ' ' + LastName FROM Employees;
    ```

  - **DATEDIFF Function**
    ```sql
    SELECT ID, FullName = FirstName + ' ' + LastName, Age = DATEDIFF(year, BirthDate, GETDATE()) FROM Employee;
    ```

  - **Math Functions**
    ```sql
    SELECT TotalCount = COUNT(MonthlySalary), 
           TotalSum = SUM(MonthlySalary),
           Average = AVG(MonthlySalary),
           MinSalary = MIN(MonthlySalary),
           MaxSalary = MAX(MonthlySalary) 
    FROM Employees;
    ```

  - **Copying data of a table to another table**
    ```sql
    SELECT *
    INTO TableCopy1
    FROM TableName;
    ```

  - **Copying only specific data**
    ```sql
    SELECT col1, col2
    INTO TableCopy2
    FROM TableName;
    ```

  - **Copying the columns of the table without data**
    ```sql
    SELECT *
    INTO TableCopy3
    FROM TableName
    WHERE 1 = 2; -- Writing a wrong condition in order to iterate on all the columns without printing any data
    ```
---------------------------------------------------------------------------------

# SQL Join

**Types:**

1. **(INNER) JOIN:** "Returns records that have matching values in both tables"

    ```sql
    -- Inner Join two Tables
    SELECT Customers.customer_id, Customers.first_name, Orders.amount
    FROM Customers
    INNER JOIN Orders
    ON Customers.customer_id = Orders.customer;
    ```

    ```sql
    -- Inner Join Three Tables with where
    SELECT Employees.ID, Employees.FirstName, Employees.LastName, Departments.Name as DeptName, Countries.Name AS CountryName
    FROM Employees 
    INNER JOIN Departments ON Employees.DepartmentID = Departments.ID 
    INNER JOIN Countries ON Employees.CountryID = Countries.ID
    WHERE Countries.Name = 'USA';
    ```

2. **LEFT (OUTER) JOIN:** "Returns all records from the left table, and the matched records from the right table"
    
    ```sql
    -- Left Join:
    SELECT Customers.CustomerID, Customers.Name, Orders.Amount
    FROM Customers 
    LEFT JOIN Orders 
    ON Customers.CustomerID = Orders.CustomerID;
    ```

3. **RIGHT (OUTER) JOIN:** "Returns all records from the right table, and the matched records from the left table"
    
    ```sql
    -- Right Join
    SELECT Customers.CustomerID, Customers.Name, Orders.Amount
    FROM Customers RIGHT OUTER JOIN
    Orders ON Customers.CustomerID = Orders.CustomerID;
    ```

4. **FULL (OUTER) JOIN:** "Returns all records when there is a match in either left or right table"

    ```sql
    -- Full Join
    SELECT Customers.CustomerID, Customers.Name, Orders.Amount
    FROM Customers FULL OUTER JOIN
    Orders ON Customers.CustomerID = Orders.CustomerID;
    ```

---------------------------------------------------------------------------------

# More SQL Queries:

**Views:**
----

- A view is a virtual table based on the result set of an SQL statement.
  
  **Example:**
  ```sql
  CREATE VIEW view_name AS
  SELECT column1, column2, ...
  FROM table_name
  WHERE condition;
  ```
  -----------------------------------------------------------------
  
**Exist:**
------------

- The EXISTS operator is used to test for the existence of any record in a subquery.
- The EXISTS operator returns TRUE if the subquery returns one or more records.  

**Example:**
```sql
SELECT * FROM Customers
WHERE EXISTS 
( 
  SELECT * FROM Orders
  WHERE customerID = Customers.CustomerID AND Amount < 600
);
```
  -----------------------------------------------------------------
  
**Union:**
-----------

- Every SELECT statement within UNION must have the same number of columns
- The columns must also have similar data types
- The columns in every SELECT statement must also be in the same order

**Example:**
```sql
SELECT column_name(s) FROM table1
UNION
SELECT column_name(s) FROM table2;
```
  -----------------------------------------------------------------

**Case:**
---------

**Example:**
```sql
SELECT ID, FirstName, LastName, GendorTitle =
CASE
  WHEN Gendor='M' THEN 'Male'
  WHEN Gendor='F' THEN 'Female'
  ELSE 'Unknown'
END
FROM Employees;
```

---------------------------------------------------------------------------------

# Operators:

**IN**
-------

  ```sql
  SELECT * FROM Employees
  WHERE DepatrmentID = 1 OR DepatrmentID = 2 OR DepatrmentID = 3 OR DepatrmentID = 5;
  ```
  or
  ```sql
  SELECT * FROM Employees
  WHERE DepatrmentID IN (1, 2, 3, 5);
  ```
   -----------------------------------------------------------------
  
**Between:**
-------

  ```sql
  Select * from Employees where
  (MonthlySalary >= 500 and MonthlySalary <= 1000);
  ```
  or
  ```sql
  Select * from Employees
  WHERE MonthlySalary Between 500 and 1000;
  ```
   -----------------------------------------------------------------
  
**LIKE**
-----

 **- Finds any values that start with "a"**
  ```sql
  select ID, FirstName from Employees
  where FirstName like 'a%';
  ```
**- Finds any values that end with “a”**
  ```sql
  select ID, FirstName from Employees
  where FirstName like '%a';
  ```
**- Finds any values that have “tell” in any position**
  ```sql
  select ID, FirstName from Employees
  where FirstName like '%tell%';
  ```
**- Finds any values that start with “a” and end with “a”**
  ```sql
  select ID, FirstName from Employees
  where FirstName like 'a%a';
  ```
**- Finds any values that have “a” in the second position**
  ```sql
  select ID, FirstName from Employees
  where FirstName like '_a%';
  ```
**- Finds any values that have “a” in the third position**
  ```sql
  select ID, FirstName from Employees
  where FirstName like '__a%';
  ```
**- Finds any values that start with “a” and are at least 3 characters in length**
  ```sql
  select ID, FirstName from Employees
  where FirstName like 'a__%';
  ```
**- Finds any values that start with “a” and are at least 4 characters in length**
  ```sql
  select ID, FirstName from Employees
  where FirstName like 'a___%';
  ```
**- Finds any values that start with “a” or “b”**
  ```sql
  select ID, FirstName from Employees
  where FirstName like 'a%' or FirstName like 'b%';
  ```
---------------------------------------------------------------------------------

# Constraints

- **Rules and conditions that are applied to the data to ensure its integrity and consistency.**

	**Types of constraints:**
  
	1. **Primary Key Constraint** -> This constraint helps to enforce data integrity and ensure that there are no duplicate rows in the table.
	2. **Foreign Key Constraint** -> This constraint establishes a relationship between two tables based on a key field.
	3. **Not Null Constraint** -> This constraint ensures that a column or set of columns cannot contain null (empty) values.
	4. **DEFAULT Constraint** -> This constraint makes a Default Value for this column if the user didn't override it or if he leaves it NULL.
	5. **Check Constraint** -> This constraint ensures that the data in a column or set of columns meets a specified condition.
	6. **Unique Constraint** -> This constraint ensures that the data in a column or set of columns is unique across all rows in the table.

	-**Difference between Primary Key Constraint and Unique Constraint**
		The primary Key is Unique but it does not allow NULL while the Unique allows NULL.
  

**Primary Key**
------------   

**Identify**

```sql
CREATE TABLE Persons (
ID int NOT NULL PRIMARY KEY,
LastName varchar(255) NOT NULL,
FirstName varchar(255),
Age int
);
```

- Or we can do it with the ALTER
```sql
ALTER TABLE Persons
ADD PRIMARY KEY (ID);
```

**Drop**
```sql
ALTER TABLE Persons
DROP CONSTRAINT PK_Person;
```
  -----------------------------------------------------------------
  
**Foreign Key**
---------

**Identify**

- This table doesn't have a foreign key
```sql
CREATE TABLE Customers (
	id INT PRIMARY KEY,
	first_name VARCHAR(40),
	last_name VARCHAR(40),
	age INT,
	country VARCHAR(10)
);
```

- Adding foreign key to the customer_id field references to the id field of the Customers table
```sql
CREATE TABLE Orders (
	order_id INT PRIMARY KEY,
	item VARCHAR(40),
	amount INT,
	customer_id INT REFERENCES Customers(id)
);
```

- Or we can do it with the ALTER
```sql
ALTER TABLE ORDERS
ADD FOREIGN KEY (customer_id) REFERENCE Customers(id);
```
  -----------------------------------------------------------------
  
**Not Null**
----------------

**Identify**
```sql
CREATE TABLE Persons (
	ID int NOT NULL,
	LastName varchar(255) NOT NULL,
	FirstName varchar(255) NOT NULL,
	Age int
);
```

- Or we can do it with the ALTER
```sql
ALTER TABLE Persons
ALTER COLUMN Age int NOT NULL;
```
  -----------------------------------------------------------------
  
**DEFAULT Constraint**
-------------

**Identify**
```sql
CREATE TABLE Persons (
	ID int NOT NULL,
	LastName varchar(255) NOT NULL,
	FirstName varchar(255),
	Age int,
	City varchar(255) DEFAULT 'Alexandria'
);
```
  
- Or we can do it with the ALTER
```sql
ALTER TABLE Persons
ADD CONSTRAINT City
DEFAULT 'Alexandria' FOR City;
```

**Drop:**
```sql
ALTER TABLE Persons
DROP Constraint City;
```
  -----------------------------------------------------------------
  
**Check Constraint**
---------------

**Identify**
```sql
CREATE TABLE Persons (
	ID int NOT NULL,
	LastName varchar(255) NOT NULL,
	FirstName varchar(255),
	Age int CHECK (Age>=18)
);
```

- Or we can do it with the ALTER
```sql
ALTER TABLE Persons
CONSTRAINT Person CHECK (Age>=18 AND City='Amman');
```

**Drop:**
```sql
ALTER TABLE Persons
DROP CONSTRAINT CHK_Person;
```
  -----------------------------------------------------------------
  
**Unique Constraint**
-------

**Identify**
```sql
CREATE TABLE Persons (
	ID int NOT NULL UNIQUE,
	LastName varchar(255) NOT NULL,
	FirstName varchar(255),
	Age int
);
```

- Or we can do it with the ALTER
```sql
ALTER TABLE Persons
ADD CONSTRAINT Person UNIQUE (ID,LastName);
```

**Drop:**
```sql
ALTER TABLE Persons
DROP CONSTRAINT UC_Person;
```
  -----------------------------------------------------------------
  
**Index**
--------------
"Indexes are used to retrieve data from the database more quickly than otherwise."

**Identify**
```sql
CREATE INDEX index_name
ON table_name (column1, column2, ...);
```

**Drop:**
```sql
DROP INDEX table_name.index_name;
```

---------------------------------------------------------------------------------

**Auto Increment:**
------------------

- We usually use it for auto-incrementing the Primary Keys

    ```sql
    CREATE TABLE Persons (
       col1 int IDENTITY(1,1) PRIMARY KEY,
       col2 varchar(255) NOT NULL,
       col3 varchar(255),
       col4 int
    );
    ```

---------------------------------------------------------------------------------    

# Normalization

- Breaking down larger databases to smaller ones to form more manageable pieces.
- Organizing the data in the database to reduce redundancy.

    **Normal Forms:**
    1. **1NF**
        - Having a Primary Key
        - Each column contains only a single value

    2. **2NF**
        - 1NF must be achieved
        - Each column in the table must be dependent on the primary key

    3. **3NF**
        - 1NF and 2NF must be achieved
        - Each column in the table must be dependent on the primary key only and not any other column

---------------------------------------------------------------------------------    

# How to use 'GUID'    **"Random choice of 5 groups of numbers"**

- `NEWID();` -> randomly change using the id

---------------------------------------------------------------------------------

# Extracting Data From a Txt file:

- **"There must be a separator between the columns of each record"**
  
1. Make a database 
2. Right-mouse click on your database and choose tasks then import a flat file

---------------------------------------------------------------------------------
