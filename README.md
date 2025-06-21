# **🛒 E-Commerce Product Category Module**

This project is a part of an E-Commerce application focusing on Product Category Management using Java, Spring Boot, and PostgreSQL. It follows a layered architecture (Controller → Service → Repository) and provides a RESTful API for managing categories.

### 📁 Project Structure

our-application/
│
├── controller/
│ 
└── CategoryController.java # Handles incoming HTTP requests
│
├── service/
│ └── CategoryService.java # Business logic for category operations
│
├── repository/
│ └── CategoryRepository.java # Interface for data persistence
│
├── model/
│ ├── Category.java # Entity class
│ └── CategoryDTO.java # DTO for transferring data
│
├── exception/
│ └── ResourceNotFoundException.java # Custom exception for not found resources
│
└── main/
└── Application.java # Spring Boot application entry point


### 🔧 Technologies Used
* Java 17
* Spring Boot 3.x* 
* Spring Data JPA
* PostgreSQL
* Lombok
* Maven
* REST API

### 📌 Features

1. Create a new category
2. Retrieve all categories with pagination and sorting
3. Update an existing category
4. Delete a category by ID

### 📡 API Endpoints

#### Category Management API

This API allows admins and public users to perform CRUD operations on categories. Below is the list of available endpoints, their methods, purposes, and required/requested data.

#### API Endpoints

| **API Name**        | **Endpoint**                              | **Method** | **Purpose**                    | **Request Body** | **Request Parameters**                       | **Response**       |
|---------------------|-------------------------------------------|------------|--------------------------------|------------------|------------------------------------------------|--------------------|
| Create Category     | `/api/admin/category`                     | POST       | Create a new category          | `Category`       | None                                           | `CategoryDTO`      |
| Get Categories      | `/api/public/categories`                  | GET        | Retrieve list of categories    | None             | `pageNumber`, `pageSize`, `sortBy`, `sortOrder` | `CategoryResponse` |
| Update Category     | `/api/admin/categories/{categoryId}`      | PUT        | Update an existing category    | `Category`       | `categoryId`                                   | `CategoryDTO`      |
| Delete Category     | `/api/admin/categories/{categoryId}`      | DELETE     | Delete an existing category    | None             | `categoryId`                                   | `CategoryDTO`      |

#### Models

#### Category (Request Body)


## 🛠️ Setup Instructions

### 1. Clone the Repository

   git clone https://github.com/your-username/ecommerce-category-module.git
   cd ecommerce-category-module

### 2. Configure Database
 Update application.properties:
spring.datasource.url=jdbc:postgresql://localhost:5432/yourdbname
spring.datasource.username=yourusername
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
✅ Make sure PostgreSQL is installed and running.

### 3. Run the Application

   ./mvnw spring-boot:run

### 4. Access the API

   Base URL: http://localhost:8080

Use Swagger UI or Postman for testing endpoints.

📦 Future Enhancements
🔐 Integrate JWT-based Authentication

🔑 Add Role-based Access (Admin vs User)

🧩 Integrate Product APIs

🌐 Build a Frontend using React or Angular

🧑‍💻 Contributors
Your Name – @your-github
