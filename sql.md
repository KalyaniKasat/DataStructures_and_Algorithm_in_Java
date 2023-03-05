# SQL TUTORIAL

## Table of Contents

1. [DBMS](#dbms)
2. [RDBMS](#rdbms) 
3. [SQL](#sql)
4. [datatypes](#data-types)
5. [Constraints](#constraints)

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




