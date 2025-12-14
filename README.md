# 🗒️ Project: Simple In-Memory To-Do List API

## 🎯 Project Goal
To gain practical experience with **Spring Boot** by creating a basic RESTful Web Service. This project focuses on using core annotations like `@SpringBootApplication`, `@RestController`, `@RequestBody`, and `@PathVariable` to handle HTTP requests and manage simple in-memory data.

## 🛠️ Required Technologies & Concepts
* **Spring Boot** (Main Application Framework)
* **REST/HTTP** (Handling GET, POST, PUT requests)
* **Spring Web Annotations** (`@RestController`, `@RequestMapping`, `@RequestBody`, `@PathVariable`)
* **POJO** (Plain Old Java Object for the data model)
* **application.properties** (Configuration)
* **Postman** (Client for testing the API)

---

## ✅ Implementation Requirements & Scoring (100 Points Total)

### I. Spring Boot Setup & Configuration (20 Points)

| Requirement | Concept Focus | Points |
| :--- | :--- | :--- |
| **1. Project Setup** | Create a Spring Boot project. Ensure the main class uses the **`@SpringBootApplication`** annotation. | 5 |
| **2. Model Definition** | Create a simple POJO, `TodoItem`, with fields: `Long id`, `String title`, and `boolean completed`. | 5 |
| **3. Property Configuration** | Utilize the **`application.properties`** file to explicitly set the application port to a non-default value (e.g., `server.port=8081`). | 10 |

---

### II. Controller & Service Logic (50 Points)

Focus on handling the core API logic and managing the in-memory data.

| Requirement | Concept Focus | Points |
| :--- | :--- | :--- |
| **4. In-Memory Storage Service** | Create a service class (e.g., `TodoService`). Manage data using a simple **`List<TodoItem>`** or **`Map<Long, TodoItem>`** within this class. The service must be **injected** into your Controller using Dependency Injection. | 10 |
| **5. POST Endpoint (Create)** | Implement a method in your **`@RestController`** (e.g., mapped to `POST /api/todos`). This method must use **`@RequestBody`** to deserialize the incoming JSON data into a new `TodoItem` and save it. | 15 |
| **6. GET Endpoint (Read All)** | Implement a method (e.g., mapped to `GET /api/todos`) that returns the entire list of `TodoItem` objects stored in the service. | 10 |
| **7. GET Endpoint (Read One)** | Implement a method (e.g., mapped to `GET /api/todos/{id}`). This method must correctly extract the ID using **`@PathVariable`** and return the matching item from the service. | 15 |

---

### III. Testing, Updates, and Error Handling (30 Points)

Validate your service and implement core update functionality.

| Requirement | Concept Focus | Points |
| :--- | :--- | :--- |
| **8. Postman Validation (CRUD)** | Successfully use **Postman** to execute the following requests: **POST** (Create) a new item, **GET** (Read All), and **GET** (Read One). *Proof of these successful API calls is required.* | 15 |
| **9. PUT Endpoint (Update)** | Implement a method (e.g., mapped to `PUT /api/todos/{id}`). This method must utilize **both** **`@PathVariable`** (for the ID) and **`@RequestBody`** (for the updated data) to find and modify an existing item in the storage. | 10 |
| **10. Basic Error Handling** | For the GET (Read One) endpoint, implement simple conditional logic to handle the case where the provided ID is **not found**, returning an appropriate HTTP status code (e.g., 404 Not Found). | 5 |

---

**Total Possible Score: 100 Points**