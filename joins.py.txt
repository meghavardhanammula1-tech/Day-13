-- GROUP BY Example
SELECT Department, SUM(Salary) AS TotalSalary
FROM Employees
GROUP BY Department;

-- HAVING Example
SELECT Department, COUNT(EmpID) AS Employee_Count
FROM Employees
GROUP BY Department
HAVING COUNT(EmpID) > 1;

-- INNER JOIN Example
SELECT StudentCourse.COURSE_ID, Student.NAME
FROM Student
INNER JOIN StudentCourse
ON Student.ROLL_NO = StudentCourse.ROLL_NO;

-- LEFT JOIN Example
SELECT Student.NAME, StudentCourse.COURSE_ID
FROM Student
LEFT JOIN StudentCourse
ON Student.ROLL_NO = StudentCourse.ROLL_NO;

-- RIGHT JOIN Example
SELECT Student.NAME, StudentCourse.COURSE_ID
FROM Student
RIGHT JOIN StudentCourse
ON Student.ROLL_NO = StudentCourse.ROLL_NO;

-- FULL JOIN Example
SELECT Student.NAME, StudentCourse.COURSE_ID
FROM Student
FULL JOIN StudentCourse
ON Student.ROLL_NO = StudentCourse.ROLL_NO;

-- NATURAL JOIN Example
SELECT Emp_name, Dept_name
FROM Employee
NATURAL JOIN Department;