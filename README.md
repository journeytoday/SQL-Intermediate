# Employee Management System

This is an Employee Management System that uses a MySQL database to store employee information such as employee ID, name, salary, department, and manager. It provides various functionalities to manage employees, such as adding new employees, updating employee information, retrieving employee insights, and managing employee hierarchy.

## Features

- Add new employees with their details such as employee ID, name, salary, department, and manager.
- Update employee information such as salary, department, and manager.
- Retrieve various employee insights, such as department-wise average salary, total number of employees in each department, highest salaried employees, lowest salaried employees, employees with the same manager, employees without a manager, and employees with at least one reportee.
- Manage employee hierarchy by tracking the manager for each employee.

## Technologies Used

- MySQL: An open-source relational database management system used to store and manage employee data.
- SQL: A standard programming language used to communicate with relational databases and perform operations such as inserting, updating, retrieving, and deleting data.

## Prerequisites

- MySQL: Install MySQL on your local machine or have access to a MySQL database server.

## Getting Started

1. Clone the repository: `git clone https://github.com/journeytoday/SQL-Intermediate.git`
2. Create a MySQL database and import the provided SQL schema to set up the required tables. You can use any MySQL client, such as MySQL Workbench or phpMyAdmin, to import the schema.
## Usage

- Add a new employee: Use the `add_employee()` function to add a new employee by providing the employee details such as ID, name, salary, department, and manager.
- Update employee information: Use the `update_employee()` function to update employee information such as salary, department, and manager by providing the employee ID and the new details.
- Retrieve employee insights: Use the various SQL queries provided in the project to retrieve employee insights such as department-wise average salary, total number of employees in each department, highest salaried employees, lowest salaried employees, employees with the same manager, employees without a manager, and employees with at least one reportee.
- Manage employee hierarchy: The application automatically tracks the manager for each employee based on the manager ID provided during employee addition or update.

## License

This project is licensed under the [MIT License](LICENSE).

## Contributing

If you would like to contribute to this project, please open an issue or submit a pull request. We welcome contributions from the community!

## Contact

For any questions or inquiries, please contact us at thejourneystoday@gmail.com

Happy Employee Management!
