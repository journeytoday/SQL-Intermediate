SQL Intermediate Operations on Dummy Database
This project demonstrates various intermediate SQL operations on a dummy database consisting of two tables: "customers" and "orders". The "customers" table contains information about customers such as customer_id, customer_name, email, city, and country. The "orders" table contains information about orders such as order_id, order_total, and customer_id.

Table Creation and Data Insertion
The project starts with the creation of tables using SQL "CREATE TABLE" statements, followed by inserting dummy data into the tables using "INSERT INTO" statements.

Intermediate SQL Operations
The project demonstrates the following intermediate SQL operations on the dummy database:

JOINS (INNER, LEFT, RIGHT, FULL): Demonstrates how to perform inner join, left join, right join, and full join between the "customers" and "orders" tables.

UNION Operator: Demonstrates how to use the UNION operator to combine the results of two SELECT statements.

SUB QUERIES: Demonstrates how to use subqueries to filter data from the "customers" table based on data from the "orders" table.

EXISTS Operator: Demonstrates how to use the EXISTS operator to filter data from the "customers" table based on the existence of related data in the "orders" table.

ANY/SOME and ALL Operators: Demonstrates how to use the ANY/SOME and ALL operators to compare a value with a set of values from the "orders" table.

IN Operator: Demonstrates how to use the IN operator to filter data from the "customers" table based on a set of values from the "orders" table.

BETWEEN Operator: Demonstrates how to use the BETWEEN operator to filter data from the "customers" table based on a range of values.

Aliases: Demonstrates how to use aliases to assign temporary names to columns or tables for ease of reference.

Views: Demonstrates how to create and use views to simplify complex queries and provide a virtual representation of the data.

Indexes: Demonstrates how to create and use indexes to improve the performance of database queries.

Constraints (NOT NULL, UNIQUE, PRIMARY KEY, FOREIGN KEY): Demonstrates how to use constraints to enforce data integrity rules on the tables, such as enforcing the uniqueness of values, defining primary and foreign keys, and ensuring that certain columns cannot contain NULL values.

Usage
Clone the repository.
Run the SQL script on your SQL server to create and populate the dummy database.
Use the SQL statements in the script to perform various intermediate SQL operations on the dummy database.
Note: Make sure to adjust the SQL statements according to the syntax and rules of the SQL server you are using.

Contribution
Contributions to this project are welcome! Feel free to submit issues, suggest improvements, or add new features.

License
This project is released under the MIT License.

Contact
For any questions or inquiries, please contact me at thejourneystoday@gmail.com
