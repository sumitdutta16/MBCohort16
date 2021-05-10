# SQL

## What is SQL ?

* SQL is a database computer language designed for the retrieval and management of data in a relational database.

* SQL stands for Structured Query Language.

## Applications Of SQL

* Allows users to access data in the relational database management systems.

* Allows users to describe the data.

* Allows users to define the data in a database and manipulate that data.

* Allows to embed within other languages using SQL modules, libraries & pre-compilers.

* Allows users to create and drop databases and tables.

## A Brief History of SQL

* **1970** - Dr. Edgar F. "Ted" Codd of IBM is known as the father of relational databases. He described a relational model for databases.

* **1974** - Structured Query Lamguage appeared.

* **1978** - IBM worked to develop Codd's ideas and released a product named System.

* **1986** - IBM developed the first prototype of relational database and standardized by ANSI. The first relational database was released by Relational Software which later came to be known as Oracle.

## SQL Process

When you are executing an SQL command for any RDBMS, the system determines the best way to carry out your request and SQL engine figures out how to interpret the task.

There are various components included in this process.

These components are −

* Query Dispatcher
* Optimization Engines
* Classic Query Engine
* SQL Query Engine, etc.

A classic query engine handles all the non-SQL queries, but a SQL query engine won't handle logical files.

Following is a simple diagram showing the SQL Architecture −

![Image](https://www.tutorialspoint.com/sql/images/sql-architecture.jpg)

***

## Categories of SQL

* **DDL (Data Definition Language) :**
DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema. It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.

> Examples of DDL commands:

| Command | Description |
| --- | --- |
| CREATE | is used to create the database or its objects. |
| DROP | is used to delete objects from the database. |
| ALTER | is used to alter structure of the database. |
| TRUNCATE | is used to remove all records from a table, including all spces allocated for the records are removed. |
| COMMENT | is used to add comments to the data dictionary. |
| RENAME | is used to rename an object existing in the database. |

***

* **DQL (Data Query Language) :**
DQL statements are used for performing queries on the data within schema objects. The purpose of the DQL Command is to get some schema relation based on the query passed to it.

> Examples of DQL commands:

| Command | Description |
| --- | --- |
| SELECT | is used to retrieve data from the database. |

***

* **DML (Data Manipulation Language) :**
The SQL commands that deals with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements.

> Examples of DML commands:

| Command | Description |
| --- | --- |
| INSERT | is used to insert data into the database. |
| UPDATE | is used to update existing data within a table |
| DELETE | is used to delete records from a database table. |

***

* **DCL (Data Control Language) :**
DCL includes commands such as GRANT and REVOKE which mainly deal with the rights, permissions and other controls of the database system.

> Examples of DCL commands:

| Command | Description |
| --- | --- |
| GRANT | gives user's access privileges to the database. |
| REVOKE | withdraw user's access privileges given by using the GRANT command. |

***

* **TCL (Transaction Control Language) :**
 TCL commands deal with the transaction within the database.

> Examples of TCL commands:

| Command | Description |
| --- | --- |
| COMMIT | commits a Transaction. |
| ROLLBACK | rollbacks a transaction in case of any eroor occurs. |
| SAVEPOINT | sets a savepoint within a transaction. |
| SET TRANSACTION | specify characteristics for the transaction. |

***

## **Various Syntax in SQL**

### SQL SELECT Statement

~~~sql
SELECT column1, column2....columnN
FROM table_name;
~~~

### SQL DISTINCT Statement

~~~sql
SELECT DISTINCT column1, column2....columnN
FROM table_name
WHERE CONDITION-1 {AND|OR} CONDITION-2;
~~~

### SQL WHERE Clause

~~~sql
SELECT column1, column2....columnN
FROM   table_name
WHERE  CONDITION;
~~~

### SQL AND/OR Clause

~~~sql
SELECT column1, column2....columnN
FROM   table_name
WHERE  CONDITION-1 {AND|OR} CONDITION-2;
~~~

### SQL IN Clause

~~~sql
SELECT column1, column2....columnN
FROM   table_name
WHERE  column_name IN (val-1, val-2,...val-N);
~~~

### SQL BETWEEN Clause

~~~sql
SELECT column1, column2....columnN
FROM   table_name
WHERE  column_name BETWEEN val-1 AND val-2;
~~~

### SQL LIKE Clause

~~~sql
SELECT column1, column2....columnN
FROM   table_name
WHERE  column_name LIKE { PATTERN };
~~~

### SQL ORDER BY Clause

~~~sql
SELECT column1, column2....columnN
FROM   table_name
WHERE  CONDITION
ORDER BY column_name {ASC|DESC};
~~~

### SQL GROUP BY Clause

~~~sql
SELECT SUM(column_name)
FROM   table_name
WHERE  CONDITION
GROUP BY column_name;
~~~

### SQL COUNT Clause

~~~sql
SELECT COUNT(column_name)
FROM   table_name
WHERE  CONDITION;
~~~

### SQL HAVING Clause

~~~sql
SELECT SUM(column_name)
FROM   table_name
WHERE  CONDITION
GROUP BY column_name
HAVING (arithematic function condition);
~~~

### SQL CREATE TABLE Statement

~~~sql
CREATE TABLE table_name(
column1 datatype,
column2 datatype,
column3 datatype,
.....
columnN datatype,
PRIMARY KEY( column_Name )
);
~~~

### SQL DROP TABLE Statement

~~~sql
DROP TABLE table_name;
~~~

### SQL CREATE INDEX Statement

~~~sql
CREATE UNIQUE INDEX index_name
ON table_name ( column1, column2,...columnN);
~~~

### SQL DROP INDEX Statement

~~~sql
ALTER TABLE table_name
DROP INDEX index_name;
~~~

### SQL DESC Statement

~~~sql
DESC table_name;
~~~

### SQL TRUNCATE TABLE Statement

~~~Sql
TRUNCATE TABLE table_name;
~~~

### SQL ALTER TABLE Statement

~~~sql
ALTER TABLE table_name {ADD|DROP|MODIFY} column_name {data_ype};
~~~

### SQL ALTER TABLE Statement (Rename)

~~~sql
ALTER TABLE table_name RENAME TO new_table_name;
~~~

### SQL INSERT INTO Statement

~~~sql
INSERT INTO table_name( column1, column2....columnN)
VALUES ( value1, value2....valueN);
~~~

### SQL UPDATE Statement

~~~sql
UPDATE table_name
SET column1 = value1, column2 = value2....columnN=valueN
[ WHERE  CONDITION ];
~~~

### SQL DELETE Statement

~~~sql
DELETE FROM table_name
WHERE  {CONDITION};
~~~

### SQL CREATE DATABASE Statement

~~~sql
CREATE DATABASE database_name;
~~~

### SQL DROP DATABASE Statement

~~~sql
DROP DATABASE database_name;
~~~

### SQL USE Statement

~~~sql
USE database_name;
~~~

### SQL COMMIT Statement

~~~sql
COMMIT;
~~~

### SQL ROLLBACK Statement

~~~sql
ROLLBACK;
~~~

***

## **SQL Join (Inner, Left, Right and Full Joins)**

A SQL Join statement is used to combine data or rows from two or more tables based on a common field between them. Different types of Joins are:

* INNER JOIN
* LEFT JOIN
* RIGHT JOIN
* FULL JOIN

Consider the two tables below:

### **Student**

| ROLL | NAME | ADDRESS | PHONE | AGE |
| --- | --- | --- | --- | --- |
| 1 | Harsh | Delhi | 1234567890 | 18 |
| 2 | Pratik | Bihar | 1234567890 | 19 |
| 3 | Riyanka | Siliguri | 1234567890 | 20 |
| 4 | Deep | Ramnagar | 1234567890 | 18 |
| 5 | Saptarhi | Kolkata | 1234567890 | 19 |
| 6 | Dhanraj | Barabajar | 1234567890 | 20 |
| 7 | Rohit | Balurghat | 1234567890 | 18 |
| 8 | Niraj | Alipur | 1234567890 | 19 |

### **StudentCourse**

| COURSE_ID | ROLL |
| --- | --- |
| 1 | 1 |
| 2 | 2 |
| 2 | 3 |
| 3 | 4 |
| 1 | 5 |
| 4 | 9 |
| 5 | 10 |
| 4 | 11 |

***

### INNER JOIN

***

The INNER JOIN keyword selects all rows from both the tables as long as the condition satisfies. This keyword will create the result-set by combining all rows from both the tables where the condition satisfies i.e value of the common field will be same.

> Syntax:

~~~sql
SELECT tableA.column1,tableA.column2,tableB.column1,....
FROM tableA 
INNER JOIN tableB
ON tableA.matching_column = tableB.matching_column;
~~~

![Inner Join Image](https://blog.codinghorror.com/content/images/uploads/2007/10/6a0120a85dcdae970b012877702708970c-pi.png)

> Example Query:

~~~sql
SELECT StudentCourse.COURSE_ID, Student.NAME, Student.AGE FROM Student
INNER JOIN StudentCourse
ON Student.ROLL_NO = StudentCourse.ROLL_NO;
~~~

> Output:

| COURSE_ID | NAME | AGE |
| --- | --- | --- |
| 1 | Amit | 18 |
| 2 | Pratik | 19 |
| 2 | Riyanka | 20 |
| 3 | Deep | 18 |
| 1 | Saptarhi | 19 |

***

### LEFT JOIN

***

This join returns all the rows of the table on the left side of the join and matching rows for the table on the right side of join. The rows for which there is no matching row on right side, the result-set will contain null. LEFT JOIN is also known as LEFT OUTER JOIN.

> Syntax:

~~~sql
SELECT tableA.column1,tableA.column2,tableB.column1,....
FROM tableA
LEFT JOIN tableB
ON tableA.matching_column = tableB.matching_column;
~~~

![LEFT Join Image](https://i.stack.imgur.com/VkAT5.png)

> Example Query:

~~~sql
SELECT Student.NAME, StudentCourse.COURSE_ID
FROM Student
LEFT JOIN StudentCourse
ON Student.ROLL_NO = StudentCourse.ROLL_NO;
~~~

> Output:

| NAME | COURSE_ID |
| --- | --- |
| Harsh | 1 |
| Pratik | 2 |
| Riyanka | 2 |
| Deep | 3 |
| Saptarhi | 1 |
| Dhanraj | NULL |
| Rohit | NULL |
| Niraj | NULL |

***

### RIGHT JOIN

***

RIGHT JOIN is similar to LEFT JOIN. This join returns all the rows of the table on the right side of the join and matching rows for the table on the left side of join. The rows for which there is no matching row on left side, the result-set will contain null. RIGHT JOIN is also known as RIGHT OUTER JOIN.

> Syntax:

~~~sql
SELECT tableA.column1,tableA.column2,tableB.column1,....
FROM tableA
RIGHT JOIN tableB
ON tableA.matching_column = tableB.matching_column;
~~~

![RIGHT Join Image](https://www.tutorialrepublic.com/lib/images/right-join.png)

> Example Query:

~~~sql
SELECT Student.NAME, StudentCourse.COURSE_ID 
FROM Student
RIGHT JOIN StudentCourse
ON Student.ROLL_NO = StudentCourse.ROLL_NO;
~~~

> Output:

| NAME | COURSE_ID |
| --- | --- |
| Harsh | 1 |
| Pratik | 2 |
| Riyanka | 2 |
| Deep | 3 |
| Saptarhi | 1 |
| NULL | 4 |
| NULL | 5 |
| NULL | 4 |

***

### FULL JOIN

***

FULL JOIN creates the result-set by combining result of both LEFT JOIN and RIGHT JOIN. The result-set will contain all the rows from both the tables. The rows for which there is no matching, the result-set will contain NULL values.

> Syntax:

~~~sql
SELECT tableA.column1,tableA.column2,tableB.column1,....
FROM tableA
FULL JOIN tableB
ON tableA.matching_column = tableB.matching_column;
~~~

![FULL Join Image](https://i.stack.imgur.com/3Ll1h.png)

> Example Query:

~~~sql
SELECT Student.NAME, StudentCourse.COURSE_ID 
FROM Student
FULL JOIN StudentCourse
ON Student.ROLL_NO = StudentCourse.ROLL_NO;
~~~

> Output:

| NAME | COURSE_ID |
| --- | --- |
| Harsh | 1 |
| Pratik | 2 |
| Riyanka | 2 |
| Deep | 3 |
| Saptarhi | 1 |
| Dhanraj | NULL |
| Rohit | NULL |
| NIRAJ | NULL |
| NULL | 9 |
| NULL | 10 |
| NULL | 11 |

***

## **SQL Aggregate Functions**

* SQL aggregation function is used to perform the calculations on multiple rows of a single column of a table. It returns a single value.

### **Types of SQL Aggregation Function**

1. **COUNT FUNCTION**
   * COUNT function is used to Count the number of rows in a database table. It can work on both numeric and non-numeric data types.
   * COUNT function uses the COUNT(*) that returns the count of all the rows in a specified table. COUNT(*) considers duplicate and Null.

    > Syntax

    ~~~sql
    COUNT(*)  
    or  
    COUNT( [ALL|DISTINCT] expression )
    ~~~

2. **SUM FUNCTION**
   * Sum function is used to calculate the sum of all selected columns. It works on numeric fields only.

    > Syntax

    ~~~sql
    SUM()  
    or  
    SUM( [ALL|DISTINCT] expression )
    ~~~

3. **AVG FUNCTION**
   * The AVG function is used to calculate the average value of the numeric type. AVG function returns the average of all non-Null values.

    > Syntax

    ~~~sql
    AVG()  
    or  
    AVG( [ALL|DISTINCT] expression )
    ~~~

4. **MAX FUNCTION**
   * MAX function is used to find the maximum value of a certain column. This function determines the largest value of all selected values of a column.

    > Syntax

    ~~~sql
    MAX()  
    or  
    MAX( [ALL|DISTINCT] expression )
    ~~~

5. **MIN FUNCTION**
   * MIN function is used to find minimum value of a certain column. This function determines the samllest value of all selected values of a column.

    > Syntax

    ~~~sql
    MIN()  
    or  
    MIN( [ALL|DISTINCT] expression )
    ~~~

***
