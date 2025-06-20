🛒 E-Commerce Product Category Module

This project is a part of an E-Commerce application focusing on Product Category Management using Java, Spring Boot, and PostgreSQL. It follows a layered architecture (Controller → Service → Repository) and provides a RESTful API for managing categories.

📁 Project Structure

our-application/
│
├── controller/
│   └── CategoryController.java
│
├── service/
│   └── CategoryService.java
│
├── repository/
│   └── CategoryRepository.java
│
├── model/
│   └── Category.java
│   └── CategoryDTO.java
│
├── exception/
│   └── ResourceNotFoundException.java
│
└── main/
    └── Application.java


🔧 Technologies Used
Java 17
Spring Boot 3.x
Spring Data JPA
PostgreSQL
Lombok
Maven
REST API

📌 Features
Create a new category
Retrieve all categories with pagination and sorting
Update an existing category
Delete a category by ID

📡 API Endpoints
API Name	Endpoint	Method	Purpose	Request Body	Request Parameters	Response
Create Category	/api/admin/category	POST	Create a new category	Category	None	CategoryDTO
Get Categories	/api/public/categories	GET	Retrieve list of categories	None	pageNumber, pageSize, sortBy, sortOrder	CategoryResponse
Update Category	/api/admin/categories/{categoryId}	PUT	Update an existing category	Category	categoryId	CategoryDTO
Delete Category	/api/admin/categories/{categoryId}	DELETE	Delete an existing category	None	categoryId	CategoryDTO

🧠 Application Architecture
Layered Architecture
Controller Layer: Handles HTTP requests.
Service Layer: Business logic and validation.
Repository Layer: Communicates with the PostgreSQL database.

Flow:

Browser (Client)
    ↓
Controller → Service → Repository → Database
    ↑
  Response Back to Client


🛠️ Setup Instructions
Clone the Repository
git clone https://github.com/your-username/ecommerce-category-module.git
cd ecommerce-category-module
Configure Database

Update application.properties:
spring.datasource.url=jdbc:postgresql://localhost:5432/yourdbname
spring.datasource.username=yourusername
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update

Run the Application
./mvnw spring-boot:run
Access API
Swagger or Postman for testing endpoints.
Server runs at http://localhost:8080

📦 Future Enhancements
Integrate Product APIs
Add JWT-based Authentication
Add Role-based Access (Admin vs User)
Frontend using React or Angular


