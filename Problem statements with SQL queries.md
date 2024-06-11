--Problem Statement 
/*
**List the salary of all the employees.**

The Employee table is described as follows:
+-------------+----------+
| Field       | Type     |
+-------------+----------+
| ENAME       | char(20) |
| ESRNO       | char(7)  |
| BDATE       | date     |
| ADDRESS     | char(20) |
| SEX         | char(20) |
| SALARY      | int(7)   |
| MGRSRNO     | char(6)  |
| DNO         | int(7)   |
+-------------+----------+
where Ename is Employee name
*/

**Solution**
```sql
SELECT ename,salary FROM employee;
```

--Problem Statement 
/*
**Display the names of all employees with any “A” at any place of the name.**

The Employee table is described as follows:
+-------------+----------+
| Field       | Type     |
+-------------+----------+
| ENAME       | char(20) |
| ESRNO       | char(7)  |
| BDATE       | date     |
| ADDRESS     | char(20) |
| SEX         | char(20) |
| SALARY      | int(7)   |
| MGRSRNO     | char(6)  |
| DNO         | int(7)   |
+-------------+----------+
*/

**Solution**
```sql
SELECT ename 
FROM employee 
WHERE ename LIKE '%A%';                 
```

--Problem Statement 
/*
**Display the name of all female employees.**

The Employee table is described as follows:
+-------------+----------+
| Field       | Type     |
+-------------+----------+
| ENAME       | char(20) |
| ESRNO       | char(7)  |
| BDATE       | date     |
| ADDRESS     | char(20) |
| SEX         | char(20) |
| SALARY      | int(7)   |
| MGRSRNO     | char(6)  |
| DNO         | int(7)   |
+-------------+----------+
*/

**Solution**
```sql
SELECT ename,sex 
FROM employee 
WHERE sex = 'F';                   
```

--Problem Statement 

**Display the employee who is paid most in the company.**

The Employee table is described as follows:

|  Field | Type |
|---|---|
| ENAME  | char(20) |
| ESRNO | char(7) |
| BDATE  | date |
| ADDRESS | char(20) |
| SEX  | char(20) |
| SALARY | int(7) |
| MGRSRNO  | char(6) |
| DNO | int(7) |


**Solution**
```sql
SELECT ename,salary 
FROM employee 
WHERE salary = (SELECT MAX(salary) FROM employee);               
```
