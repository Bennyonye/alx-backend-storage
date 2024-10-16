# 0x00. MySQL Advanced

This project focuses on advanced MySQL concepts such as creating tables with constraints, optimizing queries using indexes, and implementing stored procedures, functions, views, and triggers.

## Learning Objectives

By the end of this project, you should be able to explain the following without the help of Google:

- How to create tables with constraints.
- How to optimize queries by adding indexes.
- What are stored procedures and functions, and how to implement them in MySQL.
- What are views, and how to implement them in MySQL.
- What are triggers, and how to implement them in MySQL.

## Resources

- [MySQL cheatsheet](https://devhints.io/mysql)
- [MySQL Performance: How To Leverage MySQL Database Indexing](https://www.percona.com/blog/2021/05/20/mysql-indexing-best-practices-for-improved-performance/)
- [Stored Procedure](https://dev.mysql.com/doc/refman/8.0/en/stored-procedures.html)
- [Triggers](https://dev.mysql.com/doc/refman/8.0/en/triggers.html)
- [Views](https://dev.mysql.com/doc/refman/8.0/en/create-view.html)
- [Functions and Operators](https://dev.mysql.com/doc/refman/8.0/en/functions.html)
- [CREATE TABLE Statement](https://dev.mysql.com/doc/refman/8.0/en/create-table.html)
- [CREATE PROCEDURE and CREATE FUNCTION Statements](https://dev.mysql.com/doc/refman/8.0/en/create-procedure.html)
- [CREATE INDEX Statement](https://dev.mysql.com/doc/refman/8.0/en/create-index.html)
- [CREATE VIEW Statement](https://dev.mysql.com/doc/refman/8.0/en/create-view.html)

## Requirements

- All your files will be executed on Ubuntu 18.04 LTS using **MySQL 5.7** (version 5.7.30).
- All your files should end with a new line.
- All your SQL queries should have a comment just before them (i.e., describe the query).
- All your files should start with a comment describing the task.
- All SQL keywords should be in uppercase (e.g., `SELECT`, `WHERE`, etc.).
- A `README.md` file, at the root of the folder of the project, is mandatory.
- The length of your files will be tested using `wc`.

## Tasks

### 0. List all databases
- Write a script that lists all databases of your MySQL server.

### 1. Create a database and a table
- Write a script that creates a new database `hbtn_0d_tvshows` and a table `tv_genres` within it.

### 2. Insert values into the table
- Write a script to insert predefined genres into the `tv_genres` table.

### 3. Select data from the table
- Write a script to retrieve and display all genres from the `tv_genres` table.

### 4. Create an index
- Write a script to create an index on the `name` column in the `tv_genres` table.

### 5. Stored procedures
- Write a stored procedure to get genres by name from the `tv_genres` table.

### 6. Triggers
- Write a trigger that logs any changes made to the `tv_genres` table.

### 7. Views
- Write a script to create a view that displays the most popular genres.

## How to Use

1. Start MySQL service on your Ubuntu container:
   ```bash
   $ service mysql start
   ```

2. Run your SQL scripts using the `mysql` command:
   ```bash
   $ mysql -uroot -p < script_name.sql
   ```

3. Use the `wc` command to test file lengths:
   ```bash
   $ wc -l script_name.sql
   ```

## How to Import SQL Dump

To import an SQL dump, use the following command:

```bash
$ echo "CREATE DATABASE hbtn_0d_tvshows;" | mysql -uroot -p
$ curl "https://s3.amazonaws.com/intranet-projects-files/holbertonschool-higher-level_programming+/274/hbtn_0d_tvshows.sql" -s | mysql -uroot -p hbtn_0d_tvshows
$ echo "SELECT * FROM tv_genres" | mysql -uroot -p hbtn_0d_tvshows
```

