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
