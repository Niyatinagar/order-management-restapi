# Order Management REST API

![Java](https://img.shields.io/badge/Java-17-blue)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.2.5-brightgreen)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-blue)
![Docker](https://img.shields.io/badge/Docker-28.3-blue)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## 👩‍💻 Author

**Niyati Nagar**  
Backend Developer | Java | SQL | REST APIs  

---

## 📖 Project Overview

The **Order Management REST API** is a production-ready backend system built using **Java 17**, **Spring Boot 3**, and **PostgreSQL**.

This project simulates a real-world e-commerce order management system that handles:

- User management  
- Product inventory  
- Order processing  
- Stock deduction  
- Transaction handling  

It is designed following enterprise-level backend architecture principles such as layered structure, transactional integrity, validation, and clean RESTful API design.

---

## 🚀 Key Features

### 🔹 User Management
- Create, update, delete, and fetch users
- Unique username and email validation
- Status tracking (ACTIVE / INACTIVE)
- Audit fields (createdAt, updatedAt)

### 🔹 Product Management
- Add and manage products
- Price and stock validation
- Prevent negative stock
- SQL constraints for data integrity

### 🔹 Order Processing
- Create orders with multiple items
- Automatic stock deduction
- Atomic transactions using `@Transactional`
- Subtotal calculation per order

### 🔹 API Architecture
- RESTful endpoints
- Standardized `ApiResponse<T>` structure
- Proper HTTP status codes
- Pagination using Spring Data `Pageable`

### 🔹 Data Integrity
- Foreign key constraints
- Unique constraints
- SQL-level validations
- Enum-based status control

### 🔹 Error Handling & Logging
- Global exception handling
- Custom error responses
- SLF4J logging

### 🔹 Docker Support
- Dockerized Spring Boot application
- Docker Compose for PostgreSQL integration

---

## 🛠️ Tech Stack

- Java 17
- Spring Boot 3.2.5
- Spring Data JPA
- PostgreSQL
- Maven
- Docker & Docker Compose
- Jakarta Bean Validation
- SLF4J Logging

---

## 🏗️ Architecture Overview

This project follows a layered architecture:

Controller → Service → Repository → Database

- **Controller Layer**: Handles HTTP requests
- **Service Layer**: Contains business logic
- **Repository Layer**: Communicates with database using JPA
- **Database Layer**: PostgreSQL with constraints & indexing

---

## 📂 Project Structure

```
src/main/java/com/niyati/restapi
├── controllers
├── dtos
├── models
├── repositories
├── services
└── exceptions
```

---

## ⚙️ Running the Project (Without Docker)

1. Create PostgreSQL database:

```sql
CREATE DATABASE order_management;
```

2. Configure `application.properties`:

```
spring.datasource.url=jdbc:postgresql://localhost:5432/order_management
spring.datasource.username=postgres
spring.datasource.password=your-password
spring.jpa.hibernate.ddl-auto=update
```

3. Run the application:

```
mvn clean install
mvn spring-boot:run
```

API runs at:

```
http://localhost:8080/api/v1/
```

---

## 🐳 Running with Docker

```
mvn clean install
docker-compose up --build
```

Stop containers:

```
docker-compose down -v
```

---

## 📌 Example API

### Create User

POST `/api/v1/users`

```json
{
  "username": "niyati",
  "email": "niyati@example.com",
  "fullName": "Niyati Nagar",
  "status": "ACTIVE"
}
```

---

## 🌟 What This Project Demonstrates

- Strong understanding of REST API design
- SQL database relationships & constraints
- Transaction management using Spring
- Clean layered backend architecture
- Production-ready error handling
- Containerized deployment

---

## 🎯 Why This Project

This project reflects my ability to build scalable backend systems suitable for enterprise environments such as Oracle-based application ecosystems.

---

## 📬 Contact

**Niyati Nagar**  
GitHub: https://github.com/YOUR_USERNAME  

---

⭐ If you found this project helpful, feel free to star it!