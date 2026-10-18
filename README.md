# Student Management System - Backend API

A secure RESTful API built with Spring Boot and MySQL to manage student records. This project features stateless JWT authentication and full CRUD capabilities.

## Tech Stack
* **Java:** 26
* **Framework:** Spring Boot 4.1.1
* **Database:** MySQL 8.0.46
* **Security:** Spring Security & JWT (jjwt)
* **ORM:** Spring Data JPA / Hibernate

## Features
* **User Authentication:** Secure registration and login using JSON Web Tokens (JWT).
* **Student Management:** Create, Read, Update, and Delete (CRUD) operations for student records.
* **Role-Based Access:** API endpoints are secured and require a valid Bearer token.

## Setup Instructions
1. Clone this repository to your local machine.
2. Open MySQL Workbench and run: `CREATE DATABASE IF NOT EXISTS student_management_db;`
3. Update `src/main/resources/application.properties` with your MySQL credentials (default is `root`/`root`).
4. Run the application using IntelliJ IDEA or via the Maven wrapper: `./mvnw spring-boot:run`
5. The server will start on `http://localhost:8080`.

## API Endpoints

### Authentication (Open)
* `POST /auth/register` - Register a new user
* `POST /auth/login` - Authenticate user and receive JWT token

### Students (Secured with JWT)
* `POST /students` - Add a new student
* `GET /students` - Retrieve all students
* `GET /students/{id}` - Retrieve a specific student by ID
* `PUT /students/{id}` - Update a student's details
* `DELETE /students/{id}` - Delete a student