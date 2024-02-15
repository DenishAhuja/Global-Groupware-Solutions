# Employee Management System

This application is crafted using Spring Boot, Maven, MongoDB (NoSQL DB), and Gmail as the email service provider.

## API Endpoints

1. **Add Employee to Database:** Implement an API endpoint to add an employee to the database. The endpoint requires fields such as EmployeeName, PhoneNumber, Email, ReportsTo (referring to the Employee ID of the reporting manager), and ProfileImage (a URL to the Employee's profile image). A unique UUID is generated as the Employee ID, returned upon successful addition to the database.

2. **Get All Employees:** Implement an API endpoint to retrieve all employees from the database.

3. **Delete Employee by ID:** Implement an API endpoint to delete an employee from the database based on their ID.

4. **Update Employee by ID:** Implement an API endpoint to update an employee's details in the database based on their ID.

5. **Get nth Level Manager of an Employee:** Implement an API endpoint that, given an employee ID and a level (n), returns the nth level manager of that employee.

6. **Get Employees with Pagination and Sorting:** Modify the "Get All Employees" task to include pagination and sorting options. Clients can specify page number, page size, and sorting criteria (e.g., sort by name or email). The API returns the appropriate subset of employees based on pagination parameters.

## Prerequisites/Tools

- JDK 17
- IntelliJ or any other IDE
- MongoDB Compass
- Spring Boot knowledge
- Gitbash
- Heroku CLI
- Postman

## Setup Instructions

1. **Create Spring Boot Project:** Use Spring Initializer or your preferred IDE to create a new Spring Boot project with the specified dependencies.

2. **Add Dependencies:** Include dependencies for Spring Boot Starter Web, Spring Boot Starter Data MongoDB, Lombok, and Spring Boot Starter Mail.

3. **MongoDB Setup:**
   - Download and install MongoDB from the official MongoDB website.
   - Create a database named "emsdb" in MongoDB UI tool.

4. **Update Application Properties:** Configure MongoDB properties in the application.properties file. For email configuration, set up Gmail credentials.

## How to Run and Test

1. **Run Your Spring Boot Application:** Ensure your Spring Boot application is running locally.

2. **Open Postman:**
   - Open the Postman application on your computer.
   - Create a new request.

3. **Test Endpoints:**
   - Use the appropriate URLs for endpoints such as adding, getting, deleting, or updating employees.
   - Set request bodies for POST and PUT requests.
   - Send requests and review responses in the Postman window.

## Endpoint Details

- Add Employee: http://localhost:8080/api/employees
- Get All Employees: http://localhost:8080/api/employees
- Delete Employee by ID: http://localhost:8080/api/employees/{id}
- Update Employee by ID: http://localhost:8080/api/employees/{id}
- Get nth Level Manager: http://localhost:8080/api/employees/{employeeId}/manager/{level}
- Get Employees with Pagination and Sorting: http://localhost:8080/api/employees/paged?page={page}&pageSize={pageSize}&sortBy={sortBy}