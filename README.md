# Day-13
SQL GROUP BY, JOINS and HAVING Clause

Objective

To understand SQL GROUP BY, JOINS, and HAVING clauses and their role in data analysis and database management.

Introduction

SQL provides powerful commands to organize, combine, and filter data from database tables. GROUP BY is used to arrange data into groups, JOINS combine data from multiple tables, and HAVING filters grouped results based on aggregate conditions.

GROUP BY Clause

The GROUP BY clause groups rows that have the same values in specified columns. It is commonly used with aggregate functions such as:

- COUNT()
- SUM()
- AVG()
- MAX()
- MIN()

Example

SELECT Department, SUM(Salary) AS TotalSalary
FROM Employees
GROUP BY Department;

Benefits

- Organizes data into groups.
- Performs calculations on grouped records.
- Simplifies data analysis.

HAVING Clause

The HAVING clause filters grouped data after aggregation.

Example

SELECT Department, COUNT(EmpID) AS Employee_Count
FROM Employees
GROUP BY Department
HAVING COUNT(EmpID) > 1;

Difference Between WHERE and HAVING

WHERE| HAVING
Filters rows before grouping| Filters groups after grouping
Cannot use aggregate functions directly| Works with aggregate functions

SQL JOINS

SQL JOINS combine data from multiple tables using related columns.

Types of Joins

1. INNER JOIN

Returns only matching rows from both tables.

SELECT StudentCourse.COURSE_ID, Student.NAME
FROM Student
INNER JOIN StudentCourse
ON Student.ROLL_NO = StudentCourse.ROLL_NO;

2. LEFT JOIN

Returns all rows from the left table and matching rows from the right table.

SELECT Student.NAME, StudentCourse.COURSE_ID
FROM Student
LEFT JOIN StudentCourse
ON Student.ROLL_NO = StudentCourse.ROLL_NO;

3. RIGHT JOIN

Returns all rows from the right table and matching rows from the left table.

SELECT Student.NAME, StudentCourse.COURSE_ID
FROM Student
RIGHT JOIN StudentCourse
ON Student.ROLL_NO = StudentCourse.ROLL_NO;

4. FULL JOIN

Returns all rows from both tables.

SELECT Student.NAME, StudentCourse.COURSE_ID
FROM Student
FULL JOIN StudentCourse
ON Student.ROLL_NO = StudentCourse.ROLL_NO;

5. NATURAL JOIN

Automatically joins tables using columns with the same name.

SELECT Emp_name, Dept_name
FROM Employee
NATURAL JOIN Department;

Advantages

- Improves data retrieval efficiency.
- Combines related data from multiple tables.
- Enables advanced data analysis.
- Simplifies reporting and aggregation.

Conclusion

GROUP BY, HAVING, and JOINS are essential SQL concepts for data analysis and database operations. They help organize data, combine information from multiple tables, and filter aggregated results efficiently.
