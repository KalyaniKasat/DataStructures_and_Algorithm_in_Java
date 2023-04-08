# SQL TUTORIAL

## Table of Contents

1. [DBMS](#dbms)
2. [RDBMS](#rdbms) 
3. [SQL](#sql)
4. [datatypes](#data-types)
5. [Constraints](#constraints)
6. [SQL Language](#sql-languages)
7. [Problem set](#problem-set)
8. [Leetcode Problem Set](#leetcode-problem-set)

## DBMS 
- It stands for database management system.
- It is software which is used to maintain and manage the database.

**[1.1] Functions of DBMS**
1. Security
2. Authorization

**[1.2] Types of DBMS**
1. Relational DBMS
2. Network DBMS
3. Object Oriented DBMS
4. Hierarchical DBMS 

## RDBMS
- RDBMS stands for Relational Database Management System.
- It is type a of DBMS software where we store the data in the form of tables and relation.  
**OR**
- If DBMS software follows relational mode then it is RDBMS.       
**OR**
- If DBMS software follows EF cord rules then it is called as RDBMS.  

  
**[2.1] Relational Model**  
- It is designed by a data scientist called EF codd.
- EF cord states that all the data in relational model should be stored in a form of tables relations.
- It can store metadata.

## SQL
- SQL stands for Structured Query Language 
- It is a language which is used to communicate with RDBMS software.

**[3.1] Query language**
- It is a language which is used to communicate with DBMS software.

**[3.2] EF codd rules**  
1. Data to be entered into a cell should be single value data or atomic data.
2. We can store the data in multiple tables and we can establish connection between those two tables using key attributes.
3. To validate the table, we have to assign datatype and constraints. 
4. Datatype are mandatory but constraints are optional.

## Data types
- It is a type of data which is used to give rules to the table.

**[4.1] Types of data types**  
1. char
2. Varchar
3. Large object  
   a) char large object  
   b) binary large object  
4. Date
5. Number

**[4.1.1] char**  
- It is used to store 'A-Z' , 'a-z' , special characters , '0-9'  
*Syntax*  
  ```sql
  char(size);
  ```  
- All the datas in char data type should be written in single quote **' '**
- The unused memory in char data type is going to be wasted. 
- char data type can hold upto 2000 memory space
- It is also called as **Fixed Length Memory Allocation**

**[4.1.2] Varchar**  
- It is used to store 'A-Z' , 'a-z' , special characters , '0-9'  
*Syntax*  
  ```sql
  Varchar(size);
  ```  
- All the datas in Varchar data type should be written in single quote **' '**
- The unused memory in Varchar data type will be sent back to RAM for further usage.
- Varchar data type can hold upto 2000 memory space
- It is also called as **Variable Length Memory Allocation**  

**[4.1.3] Large object**  
1. char large object  
- It is used to store charachters in large amount  
*Syntax*  
  ```sql
  CLOB;
  ```  
- Maximum size : 4 GB  

2. binary large object  
- It is used to store multimedia files like audio, video, images etc. in binary format 
*Syntax*  
  ```sql
  BLOB;
  ```  
- Maximum size : 4 GB

**[4.1.4] Date**  
- It is used to store date in different formats.  

*Syntax*     
For past or future era
  ```sql
  'DD-MON-YYYY'
  ```    
For present era
  ```sql
  'DD-MON-YY'
  ```  
  
**[4.1.5] Number**
- It is used to store integer and decimal values.  

*Syntax*     
  ```sql
  Number(Precision [, Scale]);
  ```    
- Precision is the maximum number of integer value
- scale is number of decimal
- All the syntax written in square brackets is optional in SQL.   

## Constraints  
The conditions given to the table is called as constraints.  
**[5.1] Types of constraints**  
1. UNIQUE
2. NOT NULL
3. CHECK
4. PRIMARY KEY
5. FOREIGN KEY

**[5.1.1] UNIQUE**  
- UNIQUE is used to avoid the duplicates while entering the table.  

**[5.1.2] NOT NULL**  
- NOT NULL is constraint which is used to specify something or not empty.  

**[5.1.3] CHECK**  
- CHECK is an additional condition given to the column.  

*syntax*
```sql
   CHECK (condition);
```
**[5.1.4] Primary key**    
It is used to uniquely identify the record from the table.

characteristics of Primary key :-

- It should be UNIQUE.
- It should be NOT NULL.
- It should be combination of UNIQUE and NOT NULL.
- There should be only one primary key in a table.
- Primary key is not mandatory but designwise preferable.  

**[5.1.5] Foreign key**    
It is used to establish connection between two tables.

characteristics of Foreign key :-

- It can have duplicate values.
- It can be NULL.
- Combination of UNIQUE and NOT NULL is not required.
- Foreign is not mandatory.
- If a column wants to become foreign key it should be primary key in its own table.
- Foreign key actually belongs to parent table but stays in child table to establish the connection between those two tables.
- It is also called as **referential integrity constraint**.


## SQL Languages
1. Data Definition Language (DDL)  
2. Data Manupulation Language (DML)
3. Transactional Control Language (TCL)
4. Data Control Language (DCL)
5. Data Query Language (DQL)



## Problem set
**[7.1] QUESTIONS ON SELECTION**  

1. WRITE A QUERY TO DISPLAY THE ANNUAL SALARY OF THE EMPLOYEE WHOS NAME IS KING
```SQL
SELECT SAL*12 AS "ANNUAL SALARY"
FROM EMP
WHERE ENAME='KING';
```

2. WRITE A QUERY TO DISPLAY NAME OF THE EMPLOYEES WORKING AS CLERK
```SQL
SELECT ENAME
FROM EMP
WHERE JOB='CLERK';
```

3. WRITE A QUERY TO DISPLAY SALARY OF THE EMPLOYEES WHO ARE WORKING AS SALESMAN
``` SQL
SELECT SAL
FROM EMP
WHERE JOB='SALESMAN';
```

4. WRITE A QUERY TO DISPLAY DETAILS OF THE EMP WHO EARNS MORE THAN 2000
 ``` SQL
 SELECT *
 FROM EMP
 WHERE SAL>2000;
```

5. WRITE A QUERY TO DISPLAY DETAILS OF THE EMP WHOS NAME IS JONES
``` SQL
SELECT *
FROM EMP
WHERE ENAME='JONES';
```

6. WRITE A QUERY TO DISPLAY DETAILS OF THE EMP WHO WAS HIRED AFTER 01-JAN-81
 ``` SQL
 SELECT *
 FROM EMP
 WHERE HIREDATE>'01-JAN-81';
```

7. WRITE A QUERY TO DISPLAY NAME AND SAL ALONG WITH HIS ANNUAL SALARY IF THE ANNUAL
 SALARY IS MORE THAN 12000

``` SQL
SELECT ENAME,SAL,SAL*12 AS "ANNUAL SALARY"
FROM EMP
WHERE SAL*12 > 12000;
```

8. WRITE A QUERY TO DISPLAY EMPNO OF THE EMPLOYEES WHO ARE WORKING IN DEPT 30 
``` SQL
SELECT EMPNO
FROM EMP
WHERE DEPTNO=30;
```

9. WRITE A QUERY TO DISPLAY ENAME AND HIREDATE IF THEY ARE HIRED BEFORE 1981
``` SQL 
SELECT ENAME, HIREDATE
FROM EMP
WHERE HIREDATE<'01-JAN-1981';
```

10. WRITE A QUERY TO DISPLAY DETAILS OF THE EMPLOYEES WORKING AS MANAGER
``` SQL  
SELECT *
FROM EMP
WHERE JOB='MANAGER';
```

11. WRITE A QUERY TO DISPLAY NAME AND SALARY GIVEN TO AN EMPLOYEE IF EMPLOYEE
EARNS A COMMISSION OF RUPEES 1400 
``` SQL
SELECT ENAME,SAL
FROM EMP
WHERE COMM=1400;
```

12. WRITE A QUERY TO DISPLAY DETAILS OF EMPLOYEES HAVING COMMISSION MORE 
THAN SALARY 
``` SQL  
SELECT *
FROM EMP
WHERE COMM>SAL;
```

13. WRITE A QUERY TO DISPLAY EMPNO OF EMPLOYEES HIRED BEFORE THE YEAR 87
``` SQL  
SELECT EMPNO
FROM EMP
WHERE HIREDATE<'01-JAN-87';
```

14. WRITE A QUERY TO DISPLAY DETAILS OF EMPLOYEES WORKING AS AN ANALYST
``` SQL  
SELECT *
FROM EMP
WHERE JOB='ANALYST';
```

15. WRITE A QUERY TO DISPLAY DETAILS OF EMPS EARNING MORE THAN 2000 RUPEES PER MONTH  
``` SQL
SELECT *
FROM EMP
WHERE SAL>2000;
```


**[7.2] QUESTIONS ON GROUP BY AND HAVING CLAUSE** 

1. WRITE A QUERY TO DISPLAY TOTAL SALARY NEEDED TO PAY EACH JOB IN EMPLOYEE TABLE.
``` SQL
SELECT SUM(SAL),JOB
FROM EMP
GROUP BY JOB;
```

2. WRITE A QUERY TO DISPLAY THE HIRE DATE ON WHICH AT LEAST 3 EMPLOYEES WHERE HIRED.
``` SQL
SELECT HIREDATE
FROM EMP
GROUP BY HIREDATE
HAVING COUNT(*)>=3;
```
3. WRITE A QUERY TO DISPLAY THE DEPARTMENT NUMBER WHICH HAS MORE THAN 2 EMPLOYEES AND THE TOTAL AMOUNT REQUIRED TO PAY THE MONTHLY SALARIES OF ALL THE EMPLOYEES IN THAT DEPARTMENT SHOULD BE MORE THAN 9000.
``` SQL
SELECT DEPTNO
FROM EMP
GROUP BY DEPTNO
HAVING COUNT(*)>2 AND SUM(SAL)>9000;
```

4. WRITE A QUERY TO DISPLAY NUMBER OF EMPLOYEES WORKING IN EACH DEPARTMENT AND ITS’ AVERAGE SALARY BY EXCLUDING ALL THE EMPLOYEES WHOSE SALARY IS LESS THAN THEIR COMMISSION.
``` SQL
SELECT COUNT(*),AVG(SAL)
FROM EMP
WHERE SAL>COMM
GROUP BY DEPTNO;
```

5. WRITE A QUERY TO DISPLAY THE SALARIES WHICH HAS REPETITIONS IN THE SAL COLUMN OF EMPLOYEE TABLE.
``` SQL
SELECT SAL
FROM EMP
GROUP BY SAL
HAVING COUNT(*)>=2;
```

6. WRITE A QUERY TO DISPLAY THE EMPLOYEE NAME ONLY IF MORE THAN ONE PERSON IN THE EMPLOYEES OF THE COMPANY HAS SAME NAME.
``` SQL
SELECT ENAME
FROM EMP
GROUP BY ENAME
HAVING COUNT(*)>1;
```

7. WRITE A QUERY TO DISPLAY THE DEPARTMENT NUMBER WHOSE AVERAGE SALARY IS BETWEEN 2500 AND 3000.
``` SQL
SELECT DEPTNO,AVG(SAL)
FROM EMP
GROUP BY DEPTNO
HAVING AVG(SAL) BETWEEN 2500 AND 3000;
```

8. WRITE A QUERY TO DISPLAY THE NUMBER OF EMPLOYEES ONLY IF THEY ARE WORKING AS MANAGER OR ANALYST AND THEIR ANNUAL SAL SHOULD END WITH A ZERO, IN EACH DEPARTMENT.
``` SQL
  SELECT COUNT(*),DEPTNO
  FROM EMP
  WHERE JOB IN ('MANAGER','ANALYST') AND SAL*12 LIKE '%0'
  GROUP BY DEPTNO;
```

9. WRITE A QUERY TO DISPLAY NO OF CLERKS WORKING IN EACH DEPARTMENT.
``` SQL
SELECT COUNT(*),DEPTNO
FROM EMP
WHERE JOB='CLERK'
GROUP BY DEPTNO;
```

10. WRITE A QUERY TO DISPLAY HIGHEST SALARY GIVEN TO A MANAGER IN EACH DEPARTMENT.
``` SQL
SELECT MAX(SAL),DEPTNO
FROM EMP
WHERE JOB='MANAGER'
GROUP BY DEPTNO;
```

11. WRITE A QUERY TO DISPLAY NO OF TIMES THE SALARIES HAVE REPEATED IN THE EMP TABLE.
``` SQL
SELECT COUNT(*),SAL
FROM EMP
GROUP BY SAL;
```

12. WRITE A QUERY TO DISPLAY DEPTNO AND MUNBER OF EMPLOYEES WHORKING IN EACH DEPARTMENT EXCEPT FOR THOSE WORKING IN DEPT 10
``` SQL
SELECT DEPTNO,COUNT(*)
FROM EMP
WHERE DEPTNO NOT IN (10)
GROUP BY DEPTNO;
```

13. WAQTD NUMBER OF EMPLOYEES GETTING COMISSION IN EACH DEPARTMENT
```SQL
SELECT COUNT(*),DEPTNO
FROM EMP
WHERE COMM IS NOT NULL
GROUP BY DEPTNO;
```
14. WAQTD NUMBER OF EMPLOYEES GETTING SALARY MORE THAN 1600 EXCLUDING ALL THE MANAGERS IN EACH DEPARTEMNT
``` SQL
SELECT COUNT(*),DEPTNO
FROM EMP
WHERE SAL>1600 AND JOB NOT IN ('MANAGER')
GROUP BY DEPTNO;
```

15. WAQTD AVERAGE SALARY NEEDED TO PAY ALL THE EMPLOYEES WHO ARE HAVING A REPORTING MANAGER IN EACH JOB .
``` SQL
SELECT AVG(SAL),JOB
FROM EMP
WHERE MGR IS NOT NULL
GROUP BY JOB;
```

16. WAQTD NUMBER OF EMPLOYEES HIRED INTO THE SAME DEPARTMENT ON THE SAME DAY
``` SQL
SELECT COUNT(*),DEPTNO,HIREDATE
FROM EMP
GROUP BY DEPTNO,HIREDATE
HAVING COUNT(*)>1;
```

17. WAQTD NUMBER OF EMPLOYEES GETTING THE SAME SALARY ,WORKING IN THE SAME DEPARTMENT
``` SQL
SELECT COUNT(*),DEPTNO,SAL
FROM EMP
GROUP BY DEPTNO,SAL
HAVING COUNT(*)>1;
```

18. WAQTD MAXIMUM SALARY GIVEN IN EACH DESIGNATION EXCLUDING THOSE WHOS NAME STARTS WITH ‘K’
``` SQL
SELECT MAX(SAL),JOB
FROM EMP
WHERE ENAME NOT LIKE 'K%'
GROUP BY JOB;
```

19. WAQTD NUMBER OF EMPLOYEES REPORTING TO 7839
``` SQL
 SELECT COUNT(*)
 FROM EMP
 WHERE MGR=7839;
```

20. WAQTD NUMBER OF EMPLOYEE NAMES STARTING WITH AN VOWEL IN EACH DEPARTMENT
``` SQL
SELECT COUNT(*),DEPTNO
FROM EMP
WHERE ENAME LIKE 'A%' OR ENAME LIKE 'E%' OR ENAME LIKE 'I%' OR ENAME LIKE 'O%' OR ENAME LIKE 'U%'
GROUP BY DEPTNO;
```


**[7.2] QUESTIONS ON SUBQUERY**   

**CASE 1**
1. QUERY TO DISPLAY THE EMPLOYEE NAMES WHO ARE EARNING MORE THAN SMITH.
``` SQL
SELECT ENAME
FROM EMP
WHERE SAL> (SELECT SAL
            FROM EMP
            WHERE ENAME='SMITH')
/
```


2. QUERY TO DISPLAY ALL THE EMPLOYEES WHO’S DEPT NUMBER IS SAME AS SCOTT.
``` SQL
SELECT *
FROM EMP
WHERE DEPTNO IN (SELECT DEPTNO
            FROM EMP
            WHERE ENAME='SCOTT')
/
```


3. LIST THE EMPLOYEES WHO HAS SALARY GREATER THAN MILLER
``` SQL
SELECT *
FROM EMP
WHERE SAL > (SELECT SAL
            FROM EMP
            WHERE ENAME='MILLER')
/
```


4. WRITE A QUERY TO DISPLAY ALL THE EMPLOYEE WHOSE JOB NOT SAME AS
ALLEN AND SALARY IS GREATER THAN MARTIN
``` SQL
SELECT *
FROM EMP
WHERE JOB NOT IN (SELECT JOB
            FROM EMP
            WHERE ENAME='ALLEN') AND SAL > (SELECT SAL
                                            FROM EMP
                                            WHERE ENAME='MARTIN')
/
```


5. LIST ALL THE EMPLOYEES WHOSE JOB IS SAME AS JONES AND THEIR SALARY
LESSER THAN SCOTT
``` SQL
SELECT *
 FROM EMP
 WHERE JOB IN (SELECT JOB
               FROM EMP
               WHERE ENAME='JONES') AND SAL<(SELECT SAL
                                             FROM EMP
                                             WHERE ENAME='SCOTT')
 /
```
 

6. DISPLAY ALL THE EMPLOYEES WHO ARE JOINED AFTER BLAKE.
``` SQL
SELECT *
FROM EMP
WHERE HIREDATE>(SELECT HIREDATE
              FROM EMP
              WHERE ENAME='BLAKE')
/

```

7. WRITE A QUERY TO DISPLAY THE EMPLOYEE INFORMATION WHO IS NOT
TAKING COMMISSION AND JOINED COMPANY AFTER ALLEN.
``` SQL
SELECT *
 FROM EMP
 WHERE COMM IS NULL AND HIREDATE>(SELECT HIREDATE
                                  FROM EMP
                                  WHERE ENAME='ALLEN')
 /
```
 

8. DISPLAY DETAILS OF EMPLOYEES ALONG WITH HIKE OF 35% IN SALARY
WORKING AS PRESIDENT AND EARNING MORE THAN SMITH.
``` SQL
SELECT EMPNO,ENAME,JOB,MGR,HIREDATE,SAL,COMM,DEPTNO,SAL+SAL*35/100
FROM EMP
WHERE JOB IN 'PRESIDENT' AND SAL>(SELECT SAL
                                 FROM EMP
                                 WHERE ENAME='SMITH')
/
```


9. DISPLAY NAMES OF EMPLOYEES WHOSE COMMISSION IS MORE THAN
SALARY AND HIRED BEFORE KING.
``` SQL
SELECT ENAME
FROM EMP
WHERE COMM>SAL AND HIREDATE<(SELECT HIREDATE
                             FROM EMP
                             WHERE ENAME='KING')
/
```


10. LIST THE EMPLOYEES WHOSE DAILY SALARY IS GREATER THAN ALLEN AND 
WHO ARE JOINED BEFORE MILLER ONLY.
``` SQL
SELECT *
FROM EMP
WHERE SAL/30>(SELECT SAL/30
              FROM EMP
              WHERE ENAME IN'ALLEN') AND HIREDATE < (SELECT HIREDATE
                                                     FROM EMP
                                                     WHERE ENAME IN 'MILLER'
/
```



11. DISPLAY NUMBER OF EMPLOYEES WHOSE COMMISSION IS MORE THAN
SALARY AND EARNING MORE THAN SMITH.
``` SQL
SELECT COUNT(*)
FROM EMP
WHERE COMM>SAL AND SAL>(SELECT SAL
                        FROM EMP
                        WHERE ENAME='SMITH')
/
```


12. DISPLAY ALL THE EMPLOYEES WHOSE NAME START WITH 'S' AND HAVING
SALARY MORE THAN 'ALLEN' AND LESS THAN FORD.
``` SQL
SELECT *
FROM EMP
WHERE ENAME LIKE 'S%' AND SAL>(SELECT SAL
                               FROM EMP
                               WHERE ENAME='ALLEN') AND SAL<(SELECT SAL
                                                             FROM EMP
                                                             WHERE ENAME='FORD')
/
```


13. DISPLAY THE DEPARTMENT NAMES THAT ARE HAVING ATLEAST ONE L IN IT.
``` SQL
SELECT DNAME
FROM DEPT
WHERE DNAME LIKE '%L%';

```

14. DISPLAY THE MANAGER REPORTING,JOB AND DEPARTMENT NUMBER FOR THOSE WHO DON'T HAVE COMMISSION
``` SQL
SELECT MGR,JOB,DEPTNO
FROM EMP
WHERE COMM IS NULL;
```


**CASE 2**  
1. DISPLAY ALL THE EMPLOYEES WHOSE DEPARTMET NAMES ENDING 'S'
``` SQL
SELECT *
FROM EMP
WHERE DEPTNO IN (SELECT DEPTNO
                 FROM DEPT
                 WHERE DNAME LIKE '%S')
/
```

2. QUERY TO DISPLAY ALL THE EMPLOYEES IN 'OPERATIONS AND ACCOUNTING' DEPT.
``` SQL
SELECT *
FROM EMP
WHERE DEPTNO IN (SELECT DEPTNO
                 FROM DEPT
                 WHERE DNAME IN ('OPERATIONS','ACCOUNTING'))
/
```

3. LIST EMPLOYEES WHO LOCATED IN CHICAGO AND THEIR COMMISSION IS ZERO.
``` SQL
SELECT *
FROM EMP
WHERE DEPTNO IN (SELECT DEPTNO
                 FROM DEPT
                 WHERE LOC IN 'CHICAGO') AND COMM=0
/
```

4. LIST EMPLOYEES WHO ARE WORKING IN RESEARCH DEPARTMENT AND THEY ARE MANAGER.
``` SQL
SELECT *
FROM EMP
WHERE DEPTNO IN (SELECT DEPTNO
                 FROM DEPT
                 WHERE DNAME IN 'RESEARCH') AND JOB IN 'MANAGER'
/
```

5. DISPLAY DEPARTMENT NAME OF THE EMPLOYEES WHO EARN COMMISSION
``` SQL
SELECT DNAME
 FROM DEPT
 WHERE DEPTNO IN (SELECT DEPTNO
                  FROM EMP
                  WHERE COMM IS NOT NULL)
 /
```
 
6. DISPLAY THE DEPARTMENT NUMBER WHO WORKING IN SALES DEPARTMENT AND THEY ARE MANAGER
``` SQL
SELECT DEPTNO
FROM DEPT
WHERE DNAME IN 'SALES' AND DEPTNO IN (SELECT DEPTNO
                                      FROM EMP
                                      WHERE JOB IN 'MANAGER')
/
```


7. DISPLAY HIREDATE AND JOB OF ALL THE EMPLOYEES WORKING FOR SALES
``` SQL
SELECT HIREDATE,JOB
FROM EMP
WHERE DEPTNO IN (SELECT DEPTNO
                 FROM DEPT
                 WHERE DNAME IN 'SALES')
/
```


8. DISPLAY LOCATION AND DNAME OF EMPLOYEE WHO WORKING AS PRESIDENT
``` SQL
SELECT LOC,DNAME
FROM DEPT
WHERE DEPTNO IN (SELECT DEPTNO
                 FROM EMP
                 WHERE JOB IN 'PRESIDENT')
/
```


9. DISPLAY THE DNAME THAT ARE HAVING CLERK IN IT
``` SQL
SELECT DNAME
FROM DEPT
WHERE DEPTNO IN (SELECT DEPTNO
                 FROM EMP
                 WHERE JOB IN 'CLERK')
/
```


10. SELECT THE EMPLOYEES WHOSE DNAME IS HAVING AT LEAST TWO 'E' IN IT.
``` SQL
SELECT *
 FROM EMP
 WHERE DEPTNO IN (SELECT DEPTNO
                  FROM DEPT
                  WHERE DNAME LIKE '%E%E%')
 /
```
 

11. SELECT ALL THE EMPLOYEES WHO ARE WORKING FOR CHICAGO
``` SQL
SELECT *
FROM EMP
WHERE DEPTNO IN (SELECT DEPTNO
                 FROM DEPT
                 WHERE LOC IN 'CHICAGO')
/
```

12. LIST THE DEPARTMENT NAMES THAT ARE HAVING SALESMAN.
``` SQL
SELECT DNAME
FROM DEPT
WHERE DEPTNO IN (SELECT DEPTNO
                 FROM EMP
                 WHERE JOB IN 'SALESMAN')
/
```

13. DISPLAY THE LOCATION OF ALL THE DEAPRTMENTS WHICH HAVE EMPLOYEES JOINED IN THE YEAR 81
``` SQL
 SELECT LOC
 FROM DEPT
 WHERE DEPTNO IN (SELECT DEPTNO
                  FROM EMP
                  WHERE HIREDATE LIKE '%81')
 /
```
 

14. DISPLAY ALL THE EMPLOYEE INFORMATION WHO ARE LIVING IN A LOCATION WHICH IS HAVING AT LEAST 2 'O' IN IT.
``` SQL
SELECT *
  FROM EMP
  WHERE DEPTNO IN (SELECT DEPTNO
                   FROM DEPT
                   WHERE LOC LIKE '%O%O%')
 /
```
  

15. LIST THE NUMBER OF EMPLOYEES WHOSE JOB IS SALESMAN WORKING FOR NEWYORK AND CHICAGO
``` SQL
SELECT COUNT(*)
FROM EMP
WHERE JOB IN 'SALESMAN' AND DEPTNO IN (SELECT DEPTNO
                                       FROM DEPT
                                       WHERE LOC IN ('NEW YORK','CHICAGO'))
/
```


16. LIST THE DEPARTMENT NAMES IN WHICH THE EMPLOYEES ARE HIRED BETWEEN 1ST OF JAN 1981 AND 31ST DEC 1982 WITH SALARY MORE THAN 1800.
``` SQL
 SELECT DNAME
 FROM DEPT
 WHERE DEPTNO IN (SELECT DEPTNO
                  FROM EMP
                  WHERE HIREDATE BETWEEN '1-JAN-1981' AND '31-DEC-1982' AND SAL>1800)
 /
```
 

17. DISPLAY LOCATION OF THE EMPLOYEE WHO EARN COMMISSION
``` SQL
SELECT LOC
FROM DEPT
WHERE DEPTNO IN (SELECT DEPTNO
                 FROM EMP
                 WHERE COMM IS NOT NULL)
/
```


18. DISPLAY EMPLOYEES LOCATION WHO HAS SOME COMMISSION
``` SQL
SELECT LOC
FROM DEPT
WHERE DEPTNO IN (SELECT DEPTNO
                 FROM EMP
                 WHERE COMM IS NOT NULL)
/
```


19. DISPLAY ALL THE EMPLOYEES WHOSE JOB SAME AS 'SMITH' AND DEPARTMENT SAME AS 'JONES' AND SALARY MORE THAN 'TURNER'
``` SQL
SELECT *
FROM EMP
WHERE JOB IN (SELECT JOB
                 FROM EMP
                 WHERE ENAME IN 'SMITH') AND DEPTNO IN (SELECT DEPTNO
                                                        FROM EMP
                                                        WHERE ENAME IN 'JONES') AND SAL>(SELECT SAL
                                                                                         FROM EMP
                                                                                         WHERE ENAME IN 'TURNER')
/

```

20. SELECT ALL THE EMPLOYEES WORKING FOR DALLAS
``` SQL
SELECT *
FROM EMP
WHERE DEPTNO IN (SELECT DEPTNO
                 FROM DEPT
                 WHERE LOC IN 'DALLAS')
/
```


21. DISPLAY THE LOCATION OF AN EMPLOYEE IN ACCOUNTING DEPARTMENT.
``` SQL
SELECT LOC
FROM DEPT
WHERE DNAME IN 'ACCOUNTING';
```

22. DISPLAY THE DEPARTMENT INFORMATION OF EMPLOYEE WHO IS WORKING FOR NEW YORK LOCATION
``` SQL
SELECT *
FROM DEPT
WHERE LOC IN 'NEW YORK';
```

23. DISPLAY ALL THE CLERKS AND ANALYST WHO ARE NOT WORKING FOR 'DALLAS'
``` SQL
SELECT *
FROM EMP
WHERE JOB IN ('CLERK','ANALYST') AND DEPTNO IN (SELECT DEPTNO
                                                FROM DEPT
                                                WHERE LOC NOT IN 'DALLAS')
/
```


## Leetcode Problem Set

**[8.1] Duplicate Emails [link](https://leetcode.com/problems/duplicate-emails/description/)**

``` sql
SELECT email as Email
FROM Person
GROUP BY email
HAVING COUNT(email)>1;
```

**[8.2] Customers Who Never Order [link](https://leetcode.com/problems/customers-who-never-order/description/)**
``` sql
SELECT name AS Customers
FROM Customers
WHERE id NOT IN (SELECT customerID
                 FROM Orders);
```
**[8.3] Fix Names in a Table [link](https://leetcode.com/problems/fix-names-in-a-table/description/)**
``` sql
SELECT  user_id as user_id , INITCAP(name) as name
FROM Users
order by user_id;
```


**[8.4] Patients With a Condition [link](https://leetcode.com/problems/patients-with-a-condition/description/)**
``` sql
SELECT *
FROM Patients
WHERE conditions LIKE 'DIAB1%' OR conditions LIKE '% DIAB1%';
```

**[8.5] Combine Two Tables [link](https://leetcode.com/problems/combine-two-tables/description/)**
``` sql
SELECT firstName,lastName,city,state
FROM Person,Address
WHERE Person.personId =Address.personId (+);
```
**[8.6] Employees Earning More Than Their Managers [link](https://leetcode.com/problems/employees-earning-more-than-their-managers/description/)**
``` sql
SELECT E1.name Employee
FROM Employee E1,Employee E2
WHERE E1.managerId = E2.id AND E1.salary>E2.salary;
```
**[8.7] Delete Duplicate Emails [link](https://leetcode.com/problems/delete-duplicate-emails/description/)**
``` sql
#MySQL
DELETE p1 
FROM person p1 INNER JOIN person p2 
ON p1.email = p2.email 
WHERE p1.id > p2.id;
```
**[8.8] Employee Bonus [link](https://leetcode.com/problems/employee-bonus/description/)**
``` sql
SELECT name as name,bonus as bonus
FROM Employee,Bonus
WHERE Employee.empID=Bonus.empID(+) AND (bonus IS NULL OR bonus<1000);
```

**[8.9] Find Customer Referee [link](https://leetcode.com/problems/find-customer-referee/description/)**
``` sql
SELECT name
FROM Customer
WHERE referee_id IS NULL OR referee_id!=2;
```

**[8.10] Customer Placing the Largest Number of Orders [link](https://leetcode.com/problems/customer-placing-the-largest-number-of-orders/description/)**
``` sql
#MYSQL
SELECT customer_number
FROM Orders
GROUP BY customer_number
ORDER BY COUNT(*) DESC
LIMIT 1;
```

**[8.11]Big Countries [link](https://leetcode.com/problems/big-countries/description/)**
``` sql
#MYSQL
SELECT name,population,area
FROM World
WHERE area >= '3000000' OR population >= '25000000';
```

**[8.12]Classes More Than 5 Students [link](https://leetcode.com/problems/classes-more-than-5-students/description/)**
``` sql
#MYSQL
SELECT class
FROM Courses
GROUP BY class
HAVING COUNT(*)>=5;
```
**[8.13]Sales Person [link](https://leetcode.com/problems/sales-person/description/)**
``` sql
SELECT name
FROM SalesPerson
WHERE sales_id NOT IN (SELECT sales_id
                       FROM Orders,Company
                       WHERE Orders.com_id=Company.com_id AND name='RED');
```

