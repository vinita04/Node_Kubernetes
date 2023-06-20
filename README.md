# Node_Kubernetes

1) Database Tier : For creating MYSQL database by running statefulset.yaml and will store Database password in mysql-secret.yaml and a headless service mysql-service.yaml for accessing the database.

2) After the successful database creation then will run the below scripts for creating the Database and Database table.
    CREATE DATABASE IF NOT EXISTS EMPDATA;
        USE EMPDATA;
    CREATE TABLE EMPLOYEE (
      Emp_No INTEGER PRIMARY KEY,
      Emp_Name TEXT NOT NULL,
      Emp_Add TEXT NOT NULL,
      Emp_Phone TEXT NOT NULL,
      Dept_Name TEXT NOT NULL
    );
  
3) After creating table will execute the below script for inserting data:
    INSERT INTO EMPLOYEE VALUES (0001, 'Rahul', 'Noida','9855498465',  'Sales');
    INSERT INTO EMPLOYEE VALUES (0002, 'Suresh', 'Gurgaon','9565498495',  'IT');
    INSERT INTO EMPLOYEE VALUES (0003, 'Mahesh', 'Mumbai','9765498425',  'IT');
    INSERT INTO EMPLOYEE VALUES (0004, 'Suraj', 'Kolkata','9856549841',  'Sales');
    INSERT INTO EMPLOYEE VALUES (0005, 'Rajesh', 'Noida','9855497805', 'Finance');
    INSERT INTO EMPLOYEE VALUES (0006, 'Shyam', 'Bangalore','9855497845', 'IT');
    
4) Service API Tier : For creating microservice tier used NodeJS & ExpressJS

Link for the code repository:

Docker hub URL: 

URL for Service API tier:

5) For fetching the database configuaration have created configmap.yaml.
6) For connecting the Service API tier outside of cluser created the load-balancer-service.yaml.
7) 
