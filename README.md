# Employee Database SQL Project

A MySQL database project focused on creating and managing an Employee Management Database using SQL.

## Project Overview

This project contains three related tables:

- **Departments** – Stores department details.
- **Location** – Stores location details.
- **Employees** – Stores employee information and connects employees with their departments and locations.

## Database Schema

### Departments

| Column | Data Type | Constraints |
|---|---|---|
| department_id | INT | Primary Key |
| department_name | VARCHAR(100) | NOT NULL, UNIQUE |

### Location

| Column | Data Type | Constraints |
|---|---|---|
| location_id | INT | Primary Key, AUTO_INCREMENT |
| location | VARCHAR(30) | NOT NULL, UNIQUE |

### Employees

| Column | Data Type | Constraints |
|---|---|---|
| employee_id | INT | Primary Key |
| employee_name | VARCHAR(50) | NOT NULL |
| gender | ENUM('M','F') | Allowed values: M, F |
| age | INT | CHECK (age >= 18) |
| hire_date | DATE | DEFAULT CURRENT_DATE |
| designation | VARCHAR(100) | - |
| department_id | INT | Foreign Key |
| location_id | INT | Foreign Key |
| salary | DECIMAL(10,2) | - |

## SQL Concepts Covered

- CREATE DATABASE
- CREATE TABLE
- Primary Keys
- Foreign Keys
- NOT NULL constraints
- UNIQUE constraints
- ENUM data type
- CHECK constraints
- DEFAULT values
- AUTO_INCREMENT
- ALTER TABLE
- Adding columns
- Modifying column data types
- Dropping columns
- Renaming columns
- RENAME TABLE
- TRUNCATE TABLE
- DROP TABLE
- DROP DATABASE

## Table Relationships

The `Employees` table is connected to the `Departments` and `Location` tables using foreign keys.

- `Employees.department_id` → `Departments.department_id`
- `Employees.location_id` → `Location.location_id`

## Technologies Used

- MySQL
- SQL

## Purpose

This project was created to practice relational database design and fundamental SQL commands, including database creation, table creation, constraints, table alterations, relationships, truncation, renaming, and deletion.
