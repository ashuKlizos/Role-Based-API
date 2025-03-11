# Role-Based-API
This project is a Spring Boot REST API that provides user authentication and role-based access control (RBAC) using JWT (JSON Web Token). The API allows users to sign up, log in, and access secure endpoints based on their roles (e.g., ADMIN, USER).

🛠️ Technologies Used

Spring Boot - Framework for building Java-based applications.

Spring Security - Securing endpoints with authentication and authorization.

JWT (JSON Web Token) - Token-based authentication.

MySQL - Relational database for user storage.

Spring Data JPA - ORM for database interactions.

Maven - Build and dependency management.

IntelliJ IDEA - IDE for development.

📂 Project Structure

├── src/main/java/com/roleBasedApi
│   ├── Role_Based/API
│   │   ├── controller      # Handles API requests
│   │   ├── dto             # Data Transfer Objects
│   │   ├── entity          # JPA entities
│   │   ├── exception       # Global exception handling
│   │   ├── repository      # Database repositories
│   │   ├── security        # JWT and Spring Security setup
│   │   ├── service         # Business logic implementation
│   ├── Application.java    # Main Spring Boot application
├── src/main/resources
│   ├── application.properties  # Database and security configurations
├── pom.xml                # Maven dependencies

🚀 Features

✅ User Authentication (Signup/Login)
✅ Role-Based Access Control (RBAC) (USER, ADMIN roles)
✅ JWT-Based Authentication
✅ Secure API Endpoints
✅ Global Exception Handling
✅ Password Hashing with BCrypt
✅ MySQL Integration

📜 API Endpoints

🔹 User Authentication

HTTP Method

Endpoint

Description

POST

/api/auth/signup

User registration

POST

/api/auth/login

User login

🔹 Secure APIs (Role-Based Access)

HTTP Method

Endpoint

Role Required

Description

GET

/api/user/profile

USER / ADMIN

Get user profile

POST

/api/admin/create

ADMIN

Create new user (Admin only)

🔐 Security Implementation

User authentication with JWT

Spring Security to protect routes

JWT filters for request validation

Password hashing using BCrypt

❌ Global Exception Handling

The project implements centralized exception handling using @RestControllerAdvice.

Exceptions Handled:

InvalidRoleException

UserNotFoundException

UserExistException

Example response:

{
    "error": "Username already exists"
}

🛠️ Setup Instructions

1️⃣ Clone the Repository

git clone https://github.com/your-repo/role-based-api.git
cd role-based-api

2️⃣ Configure MySQL Database

Update application.properties:

spring.datasource.url=jdbc:mysql://localhost:3306/your_db
spring.datasource.username=root
spring.datasource.password=your_password

3️⃣ Build and Run

mvn clean install
mvn spring-boot:run

4️⃣ Test API Using Postman

Use Postman or cURL to test the endpoints.

🏆 Conclusion

This project provides a solid foundation for building secure JWT-based authentication and role-based access control systems in Spring Boot. 🚀

✉️ Need Help? Contact me via GitHub Issues.


