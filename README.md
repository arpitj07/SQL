# SQL

**This repository is a curated list of SQL commands**

```
**REFERENCE**
- [CODECADEMY](www.codecademy.com)
- [BYTESCOUT](bytescout.com) 
```

SQL, Structured Query Language, is a programming language designed to manage data stored in relational databases. SQL operates through simple, declarative statements. This keeps data accurate and secure, and it helps maintain the integrity of databases, regardless of size.


### 1.Query for Retrieving Tables
> This query can be run to retrieve the list of tables present in a database where the database is “My_Schema”.

`SELECT * FROM My_Schema.Tables;`

### 2. Query for Selecting Columns from a Table
> This is perhaps the most widely used SQL query. In the example below, we are extracting the “Student_ID” column or attribute from the table “STUDENT”.

`SELECT Student_ID FROM STUDENT;`

> If you want to display all the attributes from a particular table, this is the right query to use:

`SELECT * FROM STUDENT;`

### 3.Query for Outputting Data Using a Constraint
> This query retrieves the specified attributes from the table on the constraint Employee ID =0000

`SELECT EMP_ID, NAME FROM EMPLOYEE_TBL WHERE EMP_ID = '0000';`

### 4.Query for Outputting Sorted Data Using ‘Order By’
> This query orders the results with respect to the attribute which is referenced to using “Order By” – so for example, if that attribute is an integer data type, then the result would either be sorted in ascending or descending order; likewise, if the data type is a String then the result would be ordered in alphabetical order.

```
SELECT EMP_ID, LAST_NAME FROM EMPLOYEE
WHERE CITY = 'Seattle' ORDER BY EMP_ID;
```

> The ordering of the result can also be set manually, using “asc ” for ascending and “desc” for descending.

```
SELECT EMP_ID, LAST_NAME FROM EMPLOYEE_TBL
WHERE CITY = 'INDIANAPOLIS' ORDER BY EMP_ID asc;
```

### 5.Query for Outputting Sorted Data Using ‘Group By’
> The ‘Group By’ property groups the resulting data according to the specified attribute.

```
SELECT Name, Age FROM Patients WHERE Age > 40 
GROUP BY Age ORDER BY Name;
```



## ![#f03c15](https://placehold.it/15/f03c15/000000?text=+)   Queries for Data Manipulation Using Math Functions 

> There are a lot of built-in math functions like COUNT and AVG which provide basic functionalities of counting the number of results and averaging them respectively


### 6.Data Manipulation Using COUNT
> This query displays the total number of customers by counting each customer ID. In addition, it groups the results according to the country of each customer.

`SELECT COUNT(CustomerID), Country FROM Customers GROUP BY Country;`

### 7. Data Manipulation Using SUM
> SUM calculates the total of the attribute that is given to it as an argument.

`SELECT SUM(Salary)FROM Employee WHERE Emp_Age < 30;`

### 8. Data Manipulation Using AVG
Simple – an average of a given attribute.

`SELECT AVG(Price)FROM Products;`

### 9. ALTER TABLE
> ALTER TABLE lets you add columns to a table in a database.

```
ALTER TABLE table_name 
ADD column_name datatype;
```

### 10. AND
> AND is an operator that combines two conditions. Both conditions must be true for the row to be included in the result set.

```
SELECT column_name(s)
FROM table_name
WHERE column_1 = value_1
AND column_2 = value_2;
```

### 11. AS
> AS is a keyword in SQL that allows you to rename a column or table using an alias.

```
SELECT column_name AS 'Alias'
FROM table_name;
```

### 12. BETWEEN
> The BETWEEN operator is used to filter the result set within a certain range. The values can be numbers, text or dates.

```
SELECT column_name(s)
FROM table_name
WHERE column_name BETWEEN value_1 AND value_2;
```

### 13. CASE 
> CASE statements are used to create different outputs (usually in the SELECT statement). It is SQL's way of handling if-then logic.
```
SELECT column_name,
  CASE
    WHEN condition THEN 'Result_1'
    WHEN condition THEN 'Result_2'
    ELSE 'Result_3'
  END
FROM table_name;
```

### 14. CREATE TABLE
> CREATE TABLE creates a new table in the database. It allows you to specify the name of the table and the name of each column in the table
```
CREATE TABLE table_name (
  column_1 datatype, 
  column_2 datatype, 
  column_3 datatype
);
```

### 15. DELETE
> DELETE statements are used to remove rows from a table.
```
DELETE FROM table_name
WHERE some_column = some_value;
```

### 16. HAVING 
> HAVING was added to SQL because the WHERE keyword could not be used with aggregate functions.
```
SELECT column_name, COUNT(*)
FROM table_name
GROUP BY column_name
HAVING COUNT(*) > value;
```

### 17.  INNER JOIN
> An inner join will combine rows from different tables if the join condition is true.
```
SELECT column_name(s)
FROM table_1
JOIN table_2
ON table_1.column_name = table_2.column_name;
```

### 18. INSERT
> INSERT statements are used to add a new row to a table.
```
INSERT INTO table_name (column_1, column_2, column_3) 
VALUES (value_1, 'value_2', value_3);
```

### 19. IS NULL/ IS NOT NULL
> IS NULL and IS NOT NULL are operators used with the WHERE clause to test for empty values.
```
SELECT column_name(s)
FROM table_name
WHERE column_name IS NULL;
```

### 20. LIKE
> LIKE is a special operator used with the WHERE clause to search for a specific pattern in a column.
```
SELECT column_name(s)
FROM table_name
WHERE column_name LIKE pattern;
```

### 21. LIMIT 
> LIMIT is a clause that lets you specify the maximum number of rows the result set will have.
```
SELECT column_name(s)
FROM table_name
LIMIT number;
```

### 22. MAX()
> MAX() is a function that takes the name of a column as an argument and returns the largest value in that column.
```
SELECT MAX(column_name)
FROM table_name;
```

### 23. MIN()
> MIN() is a function that takes the name of a column as an argument and returns the smallest value in that column.
```
SELECT MIN(column_name)
FROM table_name;
```

### 24. OR
> OR is an operator that filters the result set to only include rows where either condition is true.
```
SELECT column_name
FROM table_name
WHERE column_name = value_1
OR column_name = value_2;
```

### 25. OUTER JOIN
> An outer join will combine rows from different tables even if the join condition is not met. Every row in the left table is returned in the result set, and if the join condition is not met, then NULL values are used to fill in the columns from the right table.
```
SELECT column_name(s)
FROM table_1
LEFT JOIN table_2
  ON table_1.column_name = table_2.column_name;
```

### 26. ROUND 
> ROUND() is a function that takes a column name and an integer as an argument. It rounds the values in the column to the number of decimal places specified by the integer.
```
SELECT ROUND(column_name, integer)
FROM table_name;
```

### 27. SELECT DISTINCT
> SELECT DISTINCT specifies that the statement is going to be a query that returns unique values in the specified column(s).
```
SELECT DISTINCT column_name
FROM table_name;
```

### 28. UPDATE
> UPDATE statements allow you to edit rows in a table.
```
UPDATE table_name
SET some_column = some_value
WHERE some_column = some_value;
```

### 29. WITH 
> WITH clause lets you store the result of a query in a temporary table using an alias. You can also define multiple temporary tables using a comma and with one instance of the WITH keyword.
The WITH clause is also known as common table expression (CTE) and subquery factoring.
```
WITH temporary_name AS (
   SELECT *
   FROM table_name)
SELECT *
FROM temporary_name
WHERE column_name operator value;
```


## ![#c5f015](https://placehold.it/15/c5f015/000000?text=+) Queries related to VIEW 

### 30. Query for Creating a View
> A view is a tailored table that is formed as a result of a query. It has tables and rows just like any other table. It’s usually a good idea to run queries as independent views because this allows them to be retrieved later to view the query results, rather than computing the same command every time for a particular set of results.

```
CREATE VIEW Failing_Students AS
SELECT S_NAME, Student_ID
FROM STUDENT
WHERE GPA > 40;
```

### 31. Query for Listing all Views
> This query lists all the views available in the schema.

`SELECT * FROM My_Schema.views;`

### 32. Query for Listing all Views
> This query lists all the views available in the schema.

`SELECT * FROM My_Schema.views;`

### 33. Query for Updating a View
> This query updates the view named ‘Product List’ – and if this view doesn’t exist, then the Product List view gets created as specified in this query.

```CREATE OR REPLACE VIEW [ Product List] AS
 SELECT ProductID, ProductName, Category
 FROM Products
 WHERE Discontinued = No;
 ```


### 34.  Query for Dropping a View
>This query will drop or delete a view named ‘V1’.

`DROP VIEW V1;`


### 35. Query to Display User Tables
>A user-defined table is a representation of defined information in a table, and they can be used as arguments for procedures or user-defined functions. Because they’re so useful, it’s useful to keep track of them using the following query.

`SELECT * FROM Sys.objects WHERE Type='u'`


### 36. Query to Display Primary Keys
> A primary key uniquely identifies all values within a table. The following query lists all the fields in a table’s primary key.

`SELECT * from Sys.Objects WHERE Type='PK'`


### 37. Query for Displaying Unique Keys
>A Unique Key allows a column to ensure that all of its values are different.

`SELECT * FROM Sys.Objects WHERE Type='uq'`


### 38. Displaying Foreign Keys
>Foreign keys link one table to another – they are attributes in one table which refer to the primary key of another table.

`SELECT * FROM Sys.Objects WHERE Type='f'`


### 39. Displaying Triggers
>A Trigger is sort of an ‘event listener’ – i.e, it’s a pre-specified set of instructions that execute when a certain event occurs. The list of defined triggers can be viewed using the following query.

`SELECT * FROM Sys.Objects WHERE Type='tr'`


### 40. Displaying Internal Tables
>Internal tables are formed as a by-product of a user-action and are usually not accessible. The data in internal tables cannot be manipulated; however, the metadata of the internal tables can be viewed using the following query.

`SELECT * FROM Sys.Objects WHERE Type='it'`


### 41. Displaying a List of Procedures
> A stored procedure is a group of SQL queries that logically form a single unit and perform a particular task. Thus, using the following query you can keep track of them:

`SELECT * FROM Sys.Objects WHERE Type='p'`


# SQL Queries for Advanced Users!

### 42. 






