# 🛒 sb-ecom — Spring Boot E-Commerce API

 Developed a fully functional backend REST API for an e-commerce application using Spring Boot. The project supports secure JWT-based authentication, role-based authorization, product and category management, shopping cart functionality, and order placement. Follows clean architecture with controller–service–repository layers, integrates MySQL via JPA/Hibernate, and uses Maven for build management.



---

## 🚀 Features

- 🔐 JWT-based Authentication and Role-Based Authorization
- 📦 Product and Category Management
- 🛒 Shopping Cart Functionality
- ✅ Order Placement and History
- 🧾 DTO-Based Clean API Responses
- 🔍 Pagination, Filtering, and Searching
- 📦 MySQL/PostgreSQL Support (configurable)
- ⚙️ Exception Handling and Input Validation
- 🧪 Unit and Integration Testing Support
- 🌍 RESTful API Design

---

## 🧰 Tech Stack

| Layer         | Technology                            |
|---------------|----------------------------------------|
| Backend       | Java, Spring Boot, Spring Web          |
| ORM/Database  | Spring Data JPA, Hibernate, MySQL      |
| Security      | Spring Security, JWT                   |
| Build Tool    | Maven                                  |
| Dev Tools     | Lombok, Spring Boot DevTools           |
| Validation    | Jakarta Bean Validation (JSR-380)      |
| Testing       | JUnit, Mockito                         |

---

## ⚙️ Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/tukaramchate/Ecommerce_Project.git
cd spring-boot-course/sb-ecom
```

### 2. Configure database

Update `src/main/resources/application.yml`:

```yaml
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/sb_ecom
    username: your_mysql_user
    password: your_mysql_password
  jpa:
    hibernate:
      ddl-auto: update
    show-sql: true
```

> 💡 Create the database `sb_ecom` manually in MySQL/PostgreSQL if needed.

---

### 3. Run the application

```bash
mvn spring-boot:run
```

The API will be accessible at:  
📍 `http://localhost:8080/api/`

---

## 📁 Project Structure

```
sb-ecom/
├── controller/        # API endpoints
├── service/           # Business logic
├── repository/        # Data access layer
├── model/             # Entities and DTOs
├── config/            # JWT, Security configs
├── exception/         # Global error handling
└── application.yml    # App configuration
```

---

## 🔐 Authentication

- Register and login endpoints return a JWT token.
- Use the token in the `Authorization` header for protected routes.

```http
Authorization: Bearer <your_jwt_token>
```

---

## 🧪 Running Tests

```bash
mvn test
```

---

## 📦 Example API Endpoints

| Method | Endpoint               | Description              |
|--------|------------------------|--------------------------|
| POST   | `/api/auth/register`   | Register new user        |
| POST   | `/api/auth/login`      | Authenticate and get JWT |
| GET    | `/api/products`        | Get all products         |
| POST   | `/api/cart/add`        | Add item to cart         |
| POST   | `/api/orders/place`    | Place an order           |

---

## 📌 Environment Variables (Optional)

You can externalize database and JWT secret via environment variables:

```env
DB_URL=jdbc:mysql://localhost:3306/sb_ecom
DB_USERNAME=your_mysql_user
DB_PASSWORD=your_mysql_password
JWT_SECRET=your_secret_key
```

---

## 🤝 Contribution

1. Fork the repository
2. Create your feature branch:  
   `git checkout -b feature/my-feature`
3. Commit your changes:  
   `git commit -m 'Add new feature'`
4. Push to the branch:  
   `git push origin feature/my-feature`
5. Open a Pull Request

---

## 👨‍🏫 Devloper

Devloper Name : [Tukaram Chate](https://github.com/tukaramchate)

---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
