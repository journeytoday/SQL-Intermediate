# Intermediate SQL Examples

This repository provides a collection of intermediate SQL examples for beginners who are looking to level up their SQL skills. The examples cover various SQL concepts such as JOINS (INNER, LEFT, RIGHT, FULL), UNION Operator, SUB QUERIES, EXISTS Operator, ANY/SOME and ALL Operators, IN Operator, BETWEEN Operator, Aliases, Views, Indexes, and Constraints (NOT NULL, UNIQUE, PRIMARY KEY, FOREIGN KEY).

# Dummy Database

To practice these SQL examples, a dummy database has been created with two tables: customers and orders. The customers table has the following columns: customer_id (INT), customer_name (VARCHAR(100)), email (VARCHAR(100)), city (VARCHAR(50)), and country (VARCHAR(50)). The orders table has the following columns: order_id (INT), order_total (DECIMAL(10, 2)), and customer_id (INT) as a foreign key referencing the customer_id in the customers table.

You can create these tables in your own SQL environment using the following SQL code:

-- Create customers table
CREATE TABLE customers (
    customer_id INT PRIMARY KEY,
    customer_name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE,
    city VARCHAR(50),
    country VARCHAR(50)
);

-- Create orders table
CREATE TABLE orders (
    order_id INT PRIMARY KEY,
    order_total DECIMAL(10, 2),
    customer_id INT,
    FOREIGN KEY (customer_id) REFERENCES customers (customer_id)
);
Feel free to populate the tables with your own dummy data to practice the SQL examples.

# SQL Examples

The following are some examples of intermediate SQL operations that you can practice with the dummy database:

JOINS (INNER, LEFT, RIGHT, FULL): Perform different types of joins (INNER, LEFT, RIGHT, FULL) to retrieve data from multiple tables based on matching keys.

UNION Operator: Combine the result sets of two or more SELECT statements into a single result set.

SUB QUERIES: Use subqueries to retrieve data from one table based on the results of another query.

EXISTS Operator: Use the EXISTS operator to check if a subquery returns any rows.

ANY/SOME and ALL Operators: Use the ANY/SOME and ALL operators to compare a value with a set of values returned from a subquery.

IN Operator: Use the IN operator to filter data based on a list of values.

BETWEEN Operator: Use the BETWEEN operator to filter data based on a range of values.

Aliases: Use aliases to provide temporary names for columns or tables in your SQL queries.

Views: Create and use views to simplify complex queries or to provide a layer of abstraction over the underlying tables.

Indexes: Create indexes to improve the performance of your SQL queries.

Constraints (NOT NULL, UNIQUE, PRIMARY KEY, FOREIGN KEY): Apply different types of constraints (NOT NULL, UNIQUE, PRIMARY KEY, FOREIGN KEY) to ensure data integrity and enforce business rules.

# Usage
You can clone this repository and use the SQL examples in your own SQL environment to practice and improve your intermediate SQL skills. Feel free to modify the examples or create your own scenarios to further enhance your understanding of SQL concepts.


git clone https://github.com/yourusername/intermediate-sql-examples.git

# Conclusion
Intermediate SQL operations such as JOINS, UNION Operator, SUB QUERIES, EXISTS Operator, ANY/SOME and ALL Operators, IN Operator, BETWEEN Operator, Aliases, Views, Indexes,
