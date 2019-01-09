# SQL

**This repository is a curated list of SQL commands**

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

`SELECT EMP_ID, LAST_NAME FROM EMPLOYEE
WHERE CITY = 'Seattle' ORDER BY EMP_ID;`

> The ordering of the result can also be set manually, using “asc ” for ascending and “desc” for descending.

`SELECT EMP_ID, LAST_NAME FROM EMPLOYEE_TBL
WHERE CITY = 'INDIANAPOLIS' ORDER BY EMP_ID asc;`

### 5.Query for Outputting Sorted Data Using ‘Group By’
> The ‘Group By’ property groups the resulting data according to the specified attribute.

`SELECT Name, Age FROM Patients WHERE Age > 40 
GROUP BY Age ORDER BY Name;`


### - ![#f03c15](https://placehold.it/15/f03c15/000000?text=+) Queries for Data Manipulation Using Math Functions 

> There are a lot of built-in math functions like COUNT and AVG which provide basic functionalities of counting the number of results and averaging them respectively


### 6.



