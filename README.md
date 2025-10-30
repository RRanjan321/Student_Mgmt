# Student Management CRUD App (Spring Boot + MySQL)

This is a beginner-friendly Spring Boot application for managing students. It supports basic CRUD operations (Create, Read, Update, Delete) for students with the following fields:
- id (auto-generated)
- name
- age
- sex
- address

All data is stored in a MySQL database using Spring Data JPA.

## Features
- Modern, user-friendly HTML interface (Thymeleaf)
- REST API for integration/testing (Postman, etc.)
- Clean, simple code for easy learning

## Technologies Used
- Java 17
- Spring Boot
- Spring MVC
- Spring Data JPA
- Thymeleaf
- MySQL
- Maven

## How to Run

1. **Set up MySQL:**
   - Create a database named `studentdb`.
   - Update `src/main/resources/application.properties` with your MySQL username and password:
     ```properties
     spring.datasource.url=jdbc:mysql://localhost:3306/studentdb
     spring.datasource.username=YOUR_USERNAME
     spring.datasource.password=YOUR_PASSWORD
     ```

2. **Build and Run the App:**
   - Open a terminal in the project folder.
   - Run:
     ```
     ./mvnw.cmd spring-boot:run
     ```
   - The app will start on [http://localhost:8080](http://localhost:8080)

3. **Using the Web Interface:**
   - Go to [http://localhost:8080/students](http://localhost:8080/students)
   - You can add, edit, delete, and view students using the HTML pages.

4. **Using the REST API (e.g., with Postman):**
   - Base URL: `http://localhost:8080/api/students`
   - **GET** `/api/students` — List all students
   - **GET** `/api/students/{id}` — Get a student by id
   - **POST** `/api/students` — Add a new student (JSON body, no id needed)
   - **PUT** `/api/students/{id}` — Update a student (JSON body)
   - **DELETE** `/api/students/{id}` — Delete a student

   Example POST body:
   ```json
   {
     "name": "John Doe",
     "age": 18,
     "sex": "Male",
     "address": "123 Main St"
   }
   ```

## Project Structure
- `Student.java` — JPA entity for students
- `StudentRepository.java` — JPA repository interface
- `StudentController.java` — MVC controller for HTML pages
- `StudentRestController.java` — REST API controller
- `templates/` — Thymeleaf HTML pages
- `application.properties` — MySQL and JPA configuration

## Notes
- The database schema is created/updated automatically.
- Both the web interface and REST API use the same database.
- Code is kept as simple as possible for easy understanding and learning.

---

This project is ideal for learning Spring Boot, MVC, JPA, and MySQL integration in a real-world CRUD scenario.
