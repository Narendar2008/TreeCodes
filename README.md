# GROUP BY
```java
CREATE TABLE Customer (
cust_id integer,
cname varchar(225),
Address  varchar(225),
Gender char(2),
City  varchar(225),
Pincode integer,
TotalOrdersYet integer
);

INSERT INTO Customer
VALUES 	(546, 'Rakesh Matam', 'Bongora, kamrup rural', 'M', 'Guwahati', 781015, 3),
		(1111,'Kuldeep Ravaliya','Bongora, kamrup rural','M','Guwahati', 781015, 7),
        (670,'Sugam Sehgal','Lajpat Nagar','M','Jalandhar', 144001, 2),
        (1110,'Sumit Mishra','Bongora, kamrup rural','M','Guwahati', 781015, 1),
		(890,'Lokesh Daga','Ashok Nagar','M','Jalandhar', 144003, 4),
		(700,'Riya Gupta','Dilbagh Nagar','F','Jalandhar', 144002, 5),
		(1251,'Ram Kumar','Dilbagh Nagar','M','Jalandhar', 144002, 1),
		(1300,'Shayam Singh','Ludhiana H.O','M','Ludhiana', 141001, 15),
		(245,'Neelabh Shukla','Ashok Nagar','M','Jalandhar', 144003, 10),
		(210,'Barkha Singh','Dilbagh Nagar','F','Jalandhar', 144002, 1),
		(500,'Rohan Arora','Ludhiana H.O','M','Ludhiana', 141001, 7);
```
## **Employee table**
```java
CREATE TABLE Employee
( 
	emp_id INT,
	emp_name VARCHAR(20), 
	salary INT, 
	dept_id INT,
	year_of_joining INT
);

INSERT INTO Employee VALUES(1,'sheldon',20000,10,2009);
INSERT INTO Employee VALUES(2,'amy',51000,20,2014);
INSERT INTO Employee VALUES(3,'penny',69000,30,2019);
INSERT INTO Employee VALUES(4,'leonard',88000,40,2008);
INSERT INTO Employee VALUES(5,'raj',30000,30,2015);
INSERT INTO Employee VALUES(6,'howard',40000,20,2013);
INSERT INTO Employee VALUES(7,'harvey',70000,10,2017);
INSERT INTO Employee VALUES(8,'thomas',80000,40,2010);
INSERT INTO Employee VALUES(9,'charlie',99000,10,2005);
INSERT INTO Employee VALUES(10,'alan',96000,20,2005);
```

## **Employee Table2**
```java



CREATE TABLE IF NOT EXISTS Employee_data
(
   EmpCode      integer,
   EmpFName     text,
   EmpLName     text,
   Job          text,
   Manager      text,
   HireDate     DATE,
   Salary       integer,
   DeptCode     integer
);

INSERT INTO Employee_data  
VALUES (9369, 'TONY', 'STARK', 'SOFTWARE ENGINEER', 7902, '1980-12-17', 2800,20),
       (9499, 'TIM', 'ADOLF', 'SALESMAN', 7698, '1981-02-20', 1600,30),    
       (9566, 'KIM', 'JARVIS', 'MANAGER', 7839, '1981-04-02', 3570,20),
       (9654, 'SAM', 'MILES', 'SALESMAN', 7698, '1981-09-28', 1250, 30),
       (9782, 'KEVIN', 'HILL', 'MANAGER', 7839, '1981-06-09', 2940,10),
       (9788, 'CONNIE', 'SMITH', 'ANALYST', 7566, '1982-12-09', 3000,20),
       (9839, 'ALFRED', 'KINSLEY', 'PRESIDENT', 7566, '1981-11-17', 5000, 10),
       (9844, 'PAUL', 'TIMOTHY', 'SALESMAN', 7698, '1981-09-08', 1500,30),
       (9876, 'JOHN', 'ASGHAR', 'SOFTWARE ENGINEER', 7788, '1983-01-12',3100,20),
       (9900, 'ROSE', 'SUMMERS', 'TECHNICAL LEAD', 7698, '1981-12-03', 2950, 20),
       (9902, 'ANDREW', 'FAULKNER', 'ANALYST', 7566, '1981-12-03', 3000, 10),
       (9934, 'KAREN', 'MATTHEWS', 'SOFTWARE ENGINEER', 7782, '1982-01-23', 3300,20),
       (9591, 'WENDY', 'SHAWN', 'SALESMAN', 7698, '1981-02-22', 500,30),
       (9698, 'BELLA', 'SWAN', 'MANAGER', 7839, '1981-05-01', 3420,30),
       (9777, 'MADII', 'HIMBURY', 'ANALYST', 7839, '1981-05-01', 2000, NULL),
       (9860, 'ATHENA', 'WILSON', 'ANALYST', 7839, '1992-06-21', 7000,50),
       (9861, 'JENNIFER', 'HUETTE', 'ANALYST', 7839, '1996-07-01', 5000, 50);
```

# **JOINS**
## **INNER JOIN**
```JAVA
CREATE TABLE Client_d
(
ClientID CHAR(10),
ClientFname CHAR(100),
ClientLname CHAR(100),
Age INT,
ClientEmailID CHAR(200),
PhoneNo CHAR(10),
City CHAR(20),
EmpID CHAR(5)
);

INSERT INTO Client_d
VALUES ('1','Steve','Rogers',47,'steve@avg.com','986674443','Kolkata','3'),
		('2','Dustin','Poirier',27,'dustin@ufc.com','996767643','Kolkata','3'),
		('3','Avinash','Jain',24,'avinash@leg.com','876588971','Delhi','1'),
		('4','Sushant','Aggarwal',23,'sushant@tek.com','744355585','Hyderabad','5'),
		('5','Param','Singh',36,'param@xyz.com','674445556','Mumbai','2');

CREATE TABLE Project
(
ProjectID CHAR(10),
EmpID CHAR(5),
ProjectName CHAR(200) NULL,
ProjectStartDate DATE NULL,
ClientID CHAR(10)
);

INSERT INTO Project
VALUES ('100','1','pro_1','2021-04-21','3'),
		('200','2','pro_2','2021-03-12','1'),
		('300','3','pro_3','2021-01-16','5'),
		('400','3','pro_4','2021-04-27','2'),
		('500','5','pro_5','2021-05-01','4'),
		('600','9','pro_6','2021-01-19','1'),
		('700','7','pro_7','2021-08-27','2'),
		('800','8','pro_8','2021-09-15','3');

CREATE TABLE Employee
(
EmpID CHAR(5),
EmpFname CHAR(100) NULL,
EmpLname CHAR(100) NULL,
Age INT NULL,
EmailID CHAR(200) NULL,
PhoneNo CHAR(12) NULL,
City CHAR(20) NULL 
);

INSERT INTO Employee
VALUES ('1','Riya','Khanna',21,'riya@abc.com','987655443','Delhi'),
		('2','Sahil','Kumar',32,'sahil@abc.com','987657643','Mumbai'),
		('3','Vishwas','Aanand',24,'vishwas@abc.com','987658871','Kolkata'),
		('4','Harleen','Kaur',27,'harleen@abc.com','987677585','Bengaluru'),
		('5','Priyanshu','Gupta',23,'priyanshu@abc.com','956758556','Hyderabad');
```

## LEFTOUTER JOIN
```java
CREATE TABLE Buyer(
	bid INT,
	bname VARCHAR(30),
	bcity VARCHAR(30),
	budget INT,
	sid INT 
);

CREATE TABLE Seller(
	sid INT, 
	sname VARCHAR(30),
	scity VARCHAR(30),
	profit INT
);

CREATE TABLE Product(
	pid INT,
	amount INT,
	pdate DATE, 
	bid INT,
	sid INT
);

INSERT INTO Buyer ( bid, bname, bcity, budget, sid)
VALUES (1, 'rahul', 'jammu', 1000,11), 
	 (2, 'roshni', 'chandigarh', 2000,12),
	 (3, 'ankush', 'delhi', 3000,13),
	 (4, 'himanshu', 'jaipur', 1000,14),
	 (5, 'manya', 'lucknow', 2000,11),
	 (6, 'anjali', 'dehradun', NULL,15);

INSERT INTO Seller ( sid, sname, scity, profit)
VALUES (11, 'aditi', 'delhi', 200), 
	 (12, 'anchit', 'mumbai', 300),
	 (13, 'rohit', 'chennai', 100),
	 (14, 'virat', 'kolkata', 400),
	 (15, 'taimur', 'indore', 200);

INSERT INTO Product ( pid, amount, pdate, bid, sid)
VALUES (21, 500,'2022-01-11',1,11), 
	 (22, 300,'2022-02-12',2,12),
	 (23, 1000,'2022-02-17',3,13),
	 (24, 600,'2022-03-14', 4, 14),
	 (25, 700,'2022-06-16',5,11),
	 (26, 800,'2022-08-18',6,15),
	 (27, 500,'2022-11-26',2,12);
```
# **NOTES**
### **Grouping in SQL: Overview**

Grouping in SQL involves organizing rows into groups based on common values in a column. The **`GROUP BY`** statement is central to this process, often used with **aggregate functions** to generate summary data.

---

### **Key Concepts**
1. **GROUP BY**:
   - Groups rows with identical values in specified columns.
   - Often paired with aggregate functions for summarizing data.

2. **Aggregate Functions**:
   - Perform calculations on grouped data.
     | **Function** | **Description**                     |
     |--------------|-------------------------------------|
     | `COUNT()`    | Counts the number of rows.         |
     | `AVG()`      | Calculates the average value.      |
     | `MAX()`      | Finds the maximum value.           |
     | `MIN()`      | Finds the minimum value.           |
     | `SUM()`      | Sums up the values in a column.    |

3. **General Syntax**:
   ```sql
   SELECT column_name(s), aggregate_function(column_name)
   FROM table_name
   WHERE condition
   GROUP BY column_name(s);
   ```

---

### **Examples**

#### **1. Counting Records by Group**

**Task**: Find the number of Ninjas in each city.

**Table**: `Ninjas`

| ID  | Ninja's Name   | City       |
|------|----------------|------------|
| 101  | Lokesh Ninja   | Kolkata    |
| 102  | Kuldeep Ninja  | Bhopal     |
| 103  | Raju Ninja     | Kolkata    |
| 104  | Ojasv Ninja    | Shimla     |
| 105  | Abhi Ninja     | Bhopal     |
| 106  | Tarun Ninja    | Bhopal     |

**Query**:
```sql
SELECT COUNT(ID) AS NinjaCount, City
FROM Ninjas
GROUP BY City
ORDER BY COUNT(ID) DESC;
```

**Output**:
| **NinjaCount** | **City** |
|----------------|----------|
| 3              | Bhopal   |
| 2              | Kolkata  |
| 1              | Shimla   |

---

#### **2. Filtering Groups with `HAVING` Clause**

**Task**: Find cities where the number of Ninjas is exactly 2.

**Query**:
```sql
SELECT COUNT(ID) AS NinjaCount, City
FROM Ninjas
GROUP BY City
HAVING COUNT(ID) = 2;
```

**Output**:
| **NinjaCount** | **City** |
|----------------|----------|
| 2              | Kolkata  |

---

#### **3. Using `COUNT(*)`**

**Task**: Find the total number of records in the table.

**Query**:
```sql
SELECT COUNT(*)
FROM Ninjas;
```

**Output**:
| **COUNT(*)** |
|--------------|
| 6            |

---

### **Comparison: WHERE vs. HAVING**

| **Aspect**            | **WHERE Clause**                              | **HAVING Clause**                              |
|------------------------|-----------------------------------------------|-----------------------------------------------|
| **Purpose**            | Filters rows before grouping.                | Filters groups after grouping.                |
| **Usage with GROUP BY**| Optional.                                    | Required.                                     |
| **Position**           | Before GROUP BY.                             | After GROUP BY.                               |
| **Applicable to**      | Row operations.                              | Group (column) operations.                    |
| **Statement Type**     | Can be used with SELECT, UPDATE, DELETE.      | Only used with SELECT.                        |

**Example**:
```sql
-- Using WHERE
SELECT City
FROM Ninjas
WHERE City = 'Bhopal';

-- Using HAVING
SELECT City, COUNT(*)
FROM Ninjas
GROUP BY City
HAVING City = 'Bhopal';
```

---

### **Syntax with Clause Order**

```sql
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
HAVING condition
ORDER BY column_name;
```
---

# SQL JOINS Explained

## What are JOINS in SQL?

JOINS are used in SQL to combine rows from two or more tables based on a related column between them. They are a powerful tool to query relational databases effectively.

---

## Types of JOINS

### 1. **INNER JOIN**
- **Definition**: Returns rows with matching values in both tables.
- **Syntax**:
  ```sql
  SELECT *
  FROM TableA
  INNER JOIN TableB
  ON TableA.column = TableB.column;
  ```
- **Example**:
  **Tables**:
  - `NINJA`
    | Ninja_ID | Name          | CITY     |
    |----------|---------------|----------|
    | 1        | Ojasv Ninja   | Jaipur   |
    | 2        | Tejas Ninja   | Trichy   |
    | 3        | Rejas Ninja   | Manipal  |

  - `ORDERS`
    | Order_ID | Product_name | Ninja_ID |
    |----------|--------------|----------|
    | 1        | SQL          | 1        |
    | 2        | WEBDEV       | 2        |
    | 3        | CP           | 3        |

  **Query**:
  ```sql
  SELECT Ninja_ID, Name, CITY, Product_name
  FROM NINJA
  INNER JOIN ORDERS
  ON NINJA.Ninja_ID = ORDERS.Ninja_ID;
  ```
  **Output**:
  | Ninja_ID | Name          | CITY     | Product_name |
  |----------|---------------|----------|--------------|
  | 1        | Ojasv Ninja   | Jaipur   | SQL          |
  | 2        | Tejas Ninja   | Trichy   | WEBDEV       |
  | 3        | Rejas Ninja   | Manipal  | CP           |

---

### 2. **OUTER JOIN**
#### a. **LEFT JOIN**
- **Definition**: Returns all rows from the left table and matching rows from the right table. Non-matching rows in the right table are filled with `NULL`.
- **Syntax**:
  ```sql
  SELECT *
  FROM TableA
  LEFT JOIN TableB
  ON TableA.column = TableB.column;
  ```
- **Example**:
  **Tables**: Same as above.
  **Query**:
  ```sql
  SELECT Ninja_ID, Name, CITY, Product_name
  FROM NINJA
  LEFT JOIN ORDERS
  ON NINJA.Ninja_ID = ORDERS.Ninja_ID;
  ```
  **Output**:
  | Ninja_ID | Name          | CITY     | Product_name |
  |----------|---------------|----------|--------------|
  | 1        | Ojasv Ninja   | Jaipur   | SQL          |
  | 2        | Tejas Ninja   | Trichy   | WEBDEV       |
  | 3        | Rejas Ninja   | Manipal  | CP           |
  | 5        | Kejas Ninja   | Lucknow  | NULL         |

#### b. **RIGHT JOIN**
- **Definition**: Returns all rows from the right table and matching rows from the left table. Non-matching rows in the left table are filled with `NULL`.
- **Syntax**:
  ```sql
  SELECT *
  FROM TableA
  RIGHT JOIN TableB
  ON TableA.column = TableB.column;
  ```
- **Example**: Similar to LEFT JOIN but swaps the priority of tables.

#### c. **FULL OUTER JOIN**
- **Definition**: Combines the results of both LEFT JOIN and RIGHT JOIN.
- **Syntax**:
  ```sql
  SELECT *
  FROM TableA
  FULL OUTER JOIN TableB
  ON TableA.column = TableB.column;
  ```
- **Example**:
  Combines all rows, filling `NULL` where no match exists.

---

### 3. **CROSS JOIN**
- **Definition**: Returns the Cartesian product of both tables.
- **Syntax**:
  ```sql
  SELECT *
  FROM TableA
  CROSS JOIN TableB;
  ```
- **Example**:
  For two tables with 3 rows each, the result will have \(3 \times 3 = 9\) rows.

---

### 4. **SELF JOIN**
- **Definition**: Joins a table with itself.
- **Syntax**:
  ```sql
  SELECT A.column1, B.column2
  FROM TableA A, TableA B
  WHERE A.column = B.column;
  ```
- **Example**:
  To compare rows within the same table.

---

## Notes:
1. **Optional `OUTER` Keyword**: The `OUTER` keyword is optional in `LEFT OUTER JOIN`, `RIGHT OUTER JOIN`, and `FULL OUTER JOIN`.
2. **Access All Columns**: Use `TableName.*` to retrieve all columns from a specific table.
3. **Join Interchangeability**: LEFT JOIN and RIGHT JOIN can be interchanged by reversing the table order.

---
