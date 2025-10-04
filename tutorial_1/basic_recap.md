# Getting started with mysql
- mysql install
- path - env variable
- mysql service start (if stopped)

## using cmd - connection with mysql 
    - user 
    - pass 
    - port 
    - host machine ip

## connection command
    - mysql - u user -proot --port 3306 --host localhost
    - mysql - u user -proot --port 3306
    - mysql - u user -proot --host localhost
    - mysql - u user -proot 
    

## Create Database (if not available)
    - create database db_name;
    - use db_name;
    - create table (column_name data_type, column_name data_type, column_name data_type);

Actual demonstration
```mysql
show databases;
create database tutorials;
use tutorials;
create table students(
    name varchar(25),
    age int,
    address varchar(100)
);
show tables;
select name from students;
```

## Store data into students table
```mysql
insert into students values('Ganesh', 18, 'Nagpur'); 

-- manual effort - correct column has correct value
insert into students values('bangalore', 18, 'mahesh'); 
-- error
insert into students values(19, 'pune', 'Ramesh'); 

-- Get table structure
desc students;
insert into students values('Dinesh', 17, 'Nasik'); 

insert into students(age, address, name) values(19, 'pune', 'Ramesh'); 
insert into students(address, age, name) values('bangalore', 18, 'mahesh'); 

-- Read data from table
-- show name column
select name from students;

-- show age column
select age from students;

-- show address column
select address from students;

-- show name and address column
select name, address from students;

-- show name and age column
select name, age from students;

-- show name, address and age column
select name, address, age from students;

-- show all columns
select * from students;

```

