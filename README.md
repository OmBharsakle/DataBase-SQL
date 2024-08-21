# Employee Database Management System

This repository contains SQL scripts to manage an employee database. The scripts allow you to perform various operations such as adding employees, retrieving information, updating records, and deleting employees from the database.

## Table Schema

First, create the `employees` table with the following schema:

```sql
CREATE TABLE employees (
    id INT PRIMARY KEY,
    name TEXT,
    role TEXT,
    salary INT,
    age INT,
    address TEXT,
    phone INT
);
```

## Add a New Employee
### Add a new employee with all details:
```sql
INSERT INTO employees (id, name, role, salary, age, address, phone)
VALUES (1, 'Om Bharsakle', 'Manager', 75000, 25, '101 Kailas Nagar ', '7490835410');
```
## Add Multiple Employees
### Add multiple employees with selective data:
```sql
INSERT INTO employees (id, name, role, salary)
VALUES 
(2, 'Prful', 'Developer', 65000),
(3, 'Avesh', 'Sales', 50000);
```

## Retrieve All Employees
### Retrieve all employee information:
```sql
SELECT * FROM employees;
```

## Retrieve Specific Columns
### Get specific columns for all employees (e.g., name, salary):
```sql
SELECT name, salary FROM employees;
```

## Find Employees by Role
### Find employees with a specific role (e.g., Manager):
```sql
SELECT * FROM employees WHERE role = 'Manager';
```

## Search Employees by Name
### Search for employees with names containing "An" (case-insensitive):
```sql
SELECT * FROM employees WHERE LIKE '%an%';
```

## Find Employees by Age and Salary
### Find employees older than 30 and earning more than $70,000:
```sql
SELECT * FROM employees WHERE age > 30 AND salary > 70000;
```

## Update Employee Salary
### Change the salary of an employee with ID 100:
```sql
UPDATE employees SET salary = 80000 WHERE id = 100;
```

## Update Employee Address
### Update the address for employees in the 'Sales' role:
```sql
UPDATE employees SET address = '102 Angan Recidency' WHERE role = 'Sales';
```

## Remove an Employee
### Remove an employee with ID 101:
```sql
DELETE FROM employees WHERE id = 101;
```

## Delete Employees by Age
### Delete all employees with age less than 20 (assuming it's not a valid age):
```sql
DELETE FROM employees WHERE age < 20;
```
