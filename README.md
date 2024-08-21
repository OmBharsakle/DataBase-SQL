# Employee Database Management System

This repository contains SQL scripts to manage an employee database. The scripts allow you to perform various operations such as adding employees, retrieving information, updating records, and deleting employees from the database.

## Table of Contents

- [Table Schema](#table-schema)
- [Add a New Employee](#add-a-new-employee)
- [Add Multiple Employees](#add-multiple-employees)
- [Retrieve All Employees](#retrieve-all-employees)
- [Retrieve Specific Columns](#retrieve-specific-columns)
- [Find Employees by Role](#find-employees-by-role)
- [Search Employees by Name](#search-employees-by-name)
- [Find Employees by Age and Salary](#find-employees-by-age-and-salary)
- [Update Employee Salary](#update-employee-salary)
- [Update Employee Address](#update-employee-address)
- [Remove an Employee](#remove-an-employee)
- [Delete Employees by Age](#delete-employees-by-age)

## Table Schema

First, create the `employees` table with the following schema:

```sql
CREATE TABLE employees (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    role VARCHAR(50),
    salary DECIMAL(10, 2),
    age INT,
    address VARCHAR(255),
    phone VARCHAR(15)
);
```

## Add a New Employee
### Add a new employee with all details:
```sql
INSERT INTO employees (id, name, role, salary, age, address, phone)
VALUES (1, 'John Doe', 'Manager', 75000.00, 35, '123 Main St', '123-456-7890');
```
## Add Multiple Employees
### Add multiple employees with selective data:
```sql
INSERT INTO employees (id, name, role, salary)
VALUES 
(2, 'Jane Smith', 'Developer', 65000.00),
(3, 'Emily Johnson', 'Sales', 50000.00);
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
SELECT * FROM employees WHERE LOWER(name) LIKE '%an%';
```

## Find Employees by Age and Salary
### Find employees older than 30 and earning more than $70,000:
```sql
SELECT * FROM employees WHERE age > 30 AND salary > 70000;
```

## Update Employee Salary
### Change the salary of an employee with ID 100:
```sql
UPDATE employees SET salary = 80000.00 WHERE id = 100;
```

## Update Employee Address
### Update the address for employees in the 'Sales' role:
```sql
UPDATE employees SET address = '456 New Address' WHERE role = 'Sales';
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
