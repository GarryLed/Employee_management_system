# OOP Employee Management System 
## Overview 
Build an OOP employee management system in C# with an SQL database 

## Step 1: Planning and Requirements Gathering
1. **Define the Requirements:**

- [ ] Identify the core functionalities (e.g., add, update, delete, and view employees).

- [ ] Define roles and permissions (e.g., admin, HR, employee).

- [ ] Determine data to be stored (e.g., employee ID, name, department, salary, etc.).

2. **Design the System:**

- [x] Create a high-level system architecture diagram.

The purpose of the high-level system architecture diagram is to provide an overview of the system's major components, their interactions, and the flow off data within the system. Here are the steps: 

**Step 1. Identify major components**
1. **User interface (UI)**
2. **Business Logic Layer (BLL)**
3. **Data Access Layer (DAL)**
4. **Database** 
5. **External services/systems** 

**Step 2. Define interactions between major components** 

UI<->BLL
- UI sends request to BBL (view list of current employees)
- BLL processes the request and sends back a response (confirmation message, employee list)

BLL<->DAL
- BLL calls the methods in the DAL to retrieve or update data in the database
- DAL returns confirmation of the operation to BLL 

DAL<->Database
- DAL executes queries in the database 
- Database returns the results to the DAL

BLL<->External services / systems 
- BLL interacts with external srevices or systems to integrate them into the applicaion (API's)


**Step 3. Visulize components and their interactions** 

- [ ] Draw the Components and interactions between them:

**Step 4. Review and Refine** 

#### Example of High-Level System Architecture Disgram 
- [x] Create a high-level system architecture diagram
```sql
+---------------------------------------------+
|               User Interface (UI)           |
|         Web app/ Desktop app                |
|          - Employee list view               |
|          - Add / Edit employees             |
|          - Authentacation                   |
|                                             |
|                                             |
+---------------------------------------------+
                    |
                    | User input / output 
                    v
+---------------------------------------------+
|            Business Logic Layer             |
|           - Employee Management             |
|           - Validation / Business rules     |
|           - Authentacation                  |
|                                             |
|                                             |
|                                             |
+---------------------------------------------+
                    |
                    | Data request / response 
                    v
+---------------------------------------------+
|             Data Access Layer (DAL)         |
|            - Database connection            |
|            - SQL queries                    |
|                                             |
|                                             |
|                                             |
|                                             |
+---------------------------------------------+
                    |
                    | SQL queries / results 
                    v
+---------------------------------------------+
|             Database                        |
|            - Employees                      |
|            - Departments                    |
|            - Roles                          |
|                                             |
|                                             |
|                                             |
+---------------------------------------------+
                    |
                    | External API calls 
                    v
+---------------------------------------------+
|                 External Services           |
|               - Email                       |
|               - Authentation (OAuth)                              |
|                                             |
|                                             |
|                                             |
|                                             |
+---------------------------------------------+

```


- [ ] Design the database schema.

- [ ] Plan the classes and their relationships (UML diagrams).
### Classes: 
- Employee 
- Department 
- Roles 
- 

## Step 2: Setting Up the Development Environment
- [x] Set up Visual Studio

- [ ] Set Up the Database:

Install and configure SQL Server or use a cloud-based SQL database.
Create the database and tables according to the schema.

## Step 3: Database Design
- [ ] Define the Tables:

- [ ] Create tables such as Employees, Departments, Roles, etc.
- [ ] Define relationships between tables (e.g., foreign keys).
SQL Scripts:

- [ ] Write SQL scripts to create the tables.
- [ ] Populate tables with initial data if necessary.

## Step 4: Creating the C# Project
- [x] Create a New Project:

Start a new project in Visual Studio (e.g., Windows Forms App, WPF, or ASP.NET Core depending on the interface).
- [ ] Set Up Layers:

- [ ] Data Access Layer (DAL):
- [ ] Classes to interact with the database.
- [ ] Business Logic Layer (BLL):
- [ ] Classes for business rules and operations.
- [ ] Presentation Layer (PL):
- [ ] UI components and interaction logic.

## Step 5: Implementing the Data Access Layer (DAL)
- [ ] Define Entity Classes:

- [ ] Create classes that represent database tables (e.g., Employee, Department).
- [ ] Implement Repository Pattern:

- [ ] Create interfaces and classes for data access operations (e.g., IEmployeeRepository, EmployeeRepository).
- [ ] Database Connection:

Use System.Data.SqlClient or Dapper for database connectivity.
- [ ] Implement methods for CRUD operations.

## Step 6: Implementing the Business Logic Layer (BLL)
- [ ] Define Service Interfaces:

Create interfaces for business services (e.g., IEmployeeService).
- [ ] Implement Service Classes:

- [ ] Implement the business logic in service classes (e.g., EmployeeService).
- [ ] Use dependency injection to inject repositories into service classes.

## Step 7: Implementing the Presentation Layer (PL)
- [ ] Design the User Interface:

Design forms/pages for managing employees (e.g., employee list, add employee form).
Use controls such as DataGridView, TextBoxes, Buttons, etc.
Implement UI Logic:

Bind UI controls to data sources.
Handle user interactions (e.g., button clicks, form submissions).
Validate user input.

## Step 8: Connecting the Layers
- [ ] Configure Dependency Injection:

Use a DI container (e.g., Microsoft.Extensions.DependencyInjection) to manage dependencies.
Connect UI with BLL:

Inject service classes into UI components.
Call service methods from UI event handlers.

## Step 9: Testing
Unit Testing:

- [ ] Write unit tests for business logic and data access layers.
- [ ] Use frameworks like xUnit or MSTest.
Integration Testing:

- [ ] Test the integration between layers.
- [ ] Ensure data flows correctly from UI to the database and back.
UI Testing:

- [ ] Perform manual testing to validate the user interface.
- [ ] Use automated UI testing tools if necessary.

## Step 10: Deployment and Maintenance
- [ ] Deploy the Application:

- [ ] Deploy the database to a production server.
- [ ] Publish the application using Visual Studio.
Monitoring and Maintenance:

- [ ] Monitor the application for issues.
Regularly update the application with new features and bug fixes.
