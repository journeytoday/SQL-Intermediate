# Intermediate SQL for Beginners

Welcome to the intermediate level of SQL! If you have a basic understanding of SQL and are ready to level up your skills, you've come to the right place. In this guide, we will cover several intermediate SQL concepts with examples and a dummy database for practice.

## Dummy Database
Let's start by setting up a dummy database that we will use for practicing the intermediate SQL concepts. Here are the tables we will create:


```
CREATE TABLE customers (
    customer_id INT PRIMARY KEY,
    customer_name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE,
    city VARCHAR(50),
    country VARCHAR(50)
);

CREATE TABLE orders (
    order_id INT PRIMARY KEY,
    order_total DECIMAL(10, 2),
    customer_id INT,
    FOREIGN KEY (customer_id) REFERENCES customers (customer_id)
);

```
The customers table has columns for customer_id, customer_name, email, city, and country, while the orders table has columns for order_id, order_total, and customer_id which references the customer_id column in the customers table.

## JOINS (INNER, LEFT, RIGHT, FULL)

JOINS are used to combine data from two or more tables based on a related column between them. There are several types of JOINS, including INNER JOIN, LEFT JOIN, RIGHT JOIN, and FULL JOIN.

Example of INNER JOIN:

```
SELECT c.customer_name, o.order_id, o.order_total
FROM customers c
JOIN orders o ON c.customer_id = o.customer_id;

```
Example of LEFT JOIN:

```
SELECT c.customer_name, o.order_id, o.order_total
FROM customers c
LEFT JOIN orders o ON c.customer_id = o.customer_id;

```
Example of RIGHT JOIN:

```
SELECT c.customer_name, o.order_id, o.order_total
FROM customers c
RIGHT JOIN orders o ON c.customer_id = o.customer_id;

Example of FULL JOIN:


```
SELECT c.customer_name, o.order_id, o.order_total
FROM customers c
FULL JOIN orders o ON c.customer_id = o.customer_id;

```
## UNION Operator
The UNION operator is used to combine the results of two or more SELECT statements into a single result set. The columns in the SELECT statements must have the same number of columns and compatible data types.

Example of UNION Operator:


```
SELECT customer_name, email
FROM customers
UNION
SELECT customer_name, email
FROM orders;

```
## SUB QUERIES
A subquery, also known as a nested query, is a query that is embedded within another query. It can be used to retrieve data that is then used in the outer query for further processing.

Example of SUB QUERIES:


```
SELECT customer_name
FROM customers
WHERE customer_id IN (
    SELECT customer_id
    FROM orders
    WHERE order_total > 200.00
);

```
## EXISTS Operator
The EXISTS operator is used to check if a subquery returns any rows. If the subquery returns at least one row, the EXISTS operator returns true; otherwise, it returns false.

Example of EXISTS Operator:


```
SELECT customer_name
FROM customers c
WHERE EXISTS (
    SELECT *
    FROM orders o
    WHERE o.customer_id = c.customer_id
    AND o.order_total > 200.00
);

```
## ANY/SOME and ALL Operators
The ANY/SOME and ALL operators are used to compare a value to a set of values returned by a subquery. The ANY/SOME operator returns true if the comparison is true for at least one value in the set, while the ALL operator returns true if the comparison is true for all values in the set.

Example of ANY/SOME Operator:


```
SELECT customer_name
FROM customers
WHERE order_total > ANY (
    SELECT order_total
    FROM orders
    WHERE order_date >= '2022-01-01'
);

```
Example of ALL Operator:


```
SELECT customer_name
FROM customers
WHERE order_total > ALL (
    SELECT order_total
    FROM orders
    WHERE order_date >= '2022-01-01');

```
## IN Operator
The IN operator is used to compare a value to a set of values specified in a list. It returns true if the value matches any of the values in the list.

Example of IN Operator:

```
SELECT customer_name
FROM customers
WHERE country IN ('USA', 'Canada', 'UK');

```
## BETWEEN Operator
The BETWEEN operator is used to filter data that falls within a specified range. It includes the starting and ending values in the range.

Example of BETWEEN Operator:


```
SELECT customer_name
FROM customers
WHERE order_total BETWEEN 100.00 AND 500.00;

```
## Aliases
Aliases are used to provide temporary names to tables or columns in a query. They can make the query easier to read and write.

Example of Aliases:


```
SELECT c.customer_name AS 'Name', o.order_id AS 'Order Number'
FROM customers c
JOIN orders o ON c.customer_id = o.customer_id;

```
## Views
A view is a virtual table that is created based on the result of a query. It can be used to simplify complex queries, restrict access to certain columns, or provide a simplified interface to the data.

Example of Views:


```
CREATE VIEW high_order_totals AS
SELECT customer_name, order_id, order_total
FROM customers c
JOIN orders o ON c.customer_id = o.customer_id
WHERE order_total > 500.00;

```
## Indexes
Indexes are used to improve the performance of queries by providing a faster way to look up data in a table. They can be created on one or more columns in a table to speed up searches, sorting, and filtering.

Example of Indexes:


```
CREATE INDEX idx_customer_name ON customers (customer_name);

```
## Constraints (NOT NULL, UNIQUE, PRIMARY KEY, FOREIGN KEY)
Constraints are used to define rules and requirements for the data in a table. They can be used to ensure data integrity and consistency.

```
Example of Constraints:


```
CREATE TABLE customers (
    customer_id INT PRIMARY KEY,
    customer_name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE,
    city VARCHAR(50),
    country VARCHAR(50)
);

CREATE TABLE orders (
    order_id INT PRIMARY KEY,
    order_total DECIMAL(10, 2),
    customer_id INT,
    FOREIGN KEY (customer_id) REFERENCES customers (customer_id)
);

```
That's it! You now have a basic understanding of intermediate SQL concepts. Remember, practice is key to mastering SQL, so make sure to try out these concepts on your own with the dummy database provided, and keep learning and exploring new ways to optimize your SQL queries. Happy coding!
