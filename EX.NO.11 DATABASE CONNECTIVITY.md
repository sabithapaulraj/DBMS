# Ex. No: 11 DATA BASE CONNECTIVITY USING  MYSQL AND PYTHON
### DATE : 25/10/2023 
### AIM: To create database connectivity and display the employee table 

### Steps:
1. Install mysql,visual studio,jdk, extensions of java pack.
2. Create a employee table and insert the data into employee table  
3. Create a new java project in visual studio.
4. write a java progarm to perform the following 1.create a connection 2. fetch data and store it in result set 3. Display table rows. 4. Close the connection
5. Deploy the jar file in lib folder 
6. Run the program

### Program:
```
#PROGRAM TO CONNECT MYSQL AND PYTHON
#PROGRAM CREATES A NEW DATABASE AND TABLE EMPLOYEE

#to establish connection

import mysql.connector as mc
conn=mc.connect (host='localhost', user='root',passwd='20105dsb@8516')
mycur=conn.cursor()

if conn.is_connected():
    print ("Successfully connected to MySQL")

#to create a database called EMPLOYEES

mycur.execute("DROP DATABASE IF EXISTS EMPLOYEES")
mycur.execute("Create database EMPLOYEES")
mycur.execute("Use EMPLOYEES")

#to create a table called EMPLOYEE

mycur.execute("Create table EMPLOYEE (regn int (5) NOT NULL PRIMARY KEY, NAME CHAR (20), DEPT CHAR (30), GENDER CHAR(1))")
print ("Table is created")
mycur.execute("DESC EMPLOYEE")

print("\nThe Table attributes: \n")
for i in mycur:
    print (i)

#to insert records in table EMPLOYEE
mycur.execute("INSERT INTO EMPLOYEE VALUES (10123, 'ROHIT', 'CLEANING', 'M'), (10124, 'AJAY DEV', 'ORGANISING', 'M'), (10125, 'ARCHANA', 'PACKAGING', 'F')")

#to display the table
mycur.execute("SELECT * FROM EMPLOYEE")

print("\nThe Records in the table are:")

data=mycur.fetchall()

count=mycur.rowcount

for i in data:
    print(i)

print ("Total number of rows in resultset:", count)

#END OF PROGRAM

```
### Output:
![image](https://github.com/sabithapaulraj/DBMS/assets/118343379/148951f3-d2b0-457e-92aa-09a7b1e170f5)



### Result:
Thus the database is connected and data displayed sucessfully.
