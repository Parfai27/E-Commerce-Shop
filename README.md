E-commerce Web Application
Project Overview
This project is a Mini Project for the Web Technology & Internet (INSY-413) course at the Faculty of Information Technology. It involves developing a simple e-commerce web application using Spring Boot for the backend and Thymeleaf for the frontend. The application supports both customers and admins, fulfilling the following user stories:
User Stories

Customer:
Browse products and view their details.
Add products to a shopping cart.
View the shopping cart and proceed to checkout.
Register/login to manage orders.


Admin:
Add new products and manage existing ones.
View orders and update their status.



Submission Details

Due Date: 18 May 2025
Course: Web Technology & Internet (INSY-413)
Faculty: Faculty of Information Technology
GitHub Repository: To be shared publicly and submitted via Google Classroom at:https://classroom.google.com/c/Nzc3NTAxMTgwNjMw/a/Nzc3NTAxNDA1NjEz/details

Technologies Stack

Backend: Spring Boot, Spring Data JPA, Spring Security
Frontend: Thymeleaf, Spring MVC
Styling: Bootstrap (or Material-UI)
Database: MySQL or PostgreSQL
Build Tool: Maven

Features
Backend (Spring Boot) - 7 Points

Role-based access control with USER and ADMIN roles using Spring Security.
CRUD APIs for product management with entities (Product) and repositories.
Order management APIs (place orders, view history) with entities (Order) and relationships.
RESTful APIs for frontend interaction, using proper HTTP methods (GET, POST, PUT, DELETE) with JSON responses.
Server-side validation using Spring validations.

Frontend (Thymeleaf) - 18 Points

UI components for product browsing, shopping cart, order management, and user authentication.
Styled with Bootstrap for a responsive design.
Integration with backend APIs to fetch products, authenticate users, and manage orders.
Login and signup forms integrated with Spring Security.
Features to add/remove products to/from the cart, calculate totals, and handle checkout.
Management of static resources (CSS, JavaScript) for styling and interactivity.

Additional Requirements - 15 Points

Error handling mechanisms for both backend and frontend.
Display meaningful error messages to users.
Deploy the application on a cloud platform (e.g., Heroku, AWS, or Azure).
Source code and documentation hosted publicly on GitHub.
Share the GitHub repository link via Google Classroom.

Prerequisites
To set up and run this project, ensure you have the following installed:

Java 17 or later
Maven (for dependency management)
MySQL or PostgreSQL (database)
Git (to clone the repository)
An IDE like IntelliJ IDEA or Eclipse (optional but recommended)

Project Setup Instructions
1. Create a New Spring Boot Project

Use Spring Initializr to generate a Spring Boot project.
Select Maven as the build tool.
Add dependencies: Spring Web, Spring Data JPA, Spring Security, Thymeleaf, and a database driver (e.g., MySQL).

2. Configure Database Connectivity

Set up a MySQL or PostgreSQL database.
Create a database named ecommerce_db.
Update src/main/resources/application.properties with your database credentials:spring.datasource.url=jdbc:mysql://localhost:3306/ecommerce_db
spring.datasource.username=root
spring.datasource.password=your_password
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true



3. Use Spring Data JPA

Define entities: Product, Order, and User.
Create repositories extending JpaRepository for database operations.

4. Implement Spring Security

Define roles (USER, ADMIN) in the database.
Configure Spring Security to restrict access based on roles.
Set up authentication endpoints for login and registration.

Steps to Run the Project Locally
1. Clone the Repository
Clone this repository to your local machine:
git clone https://github.com/<your-username>/e-commerce-web-app.git

2. Navigate to the Project Directory
cd e-commerce-web-app

3. Configure the Database

Ensure your MySQL or PostgreSQL server is running.
Update application.properties with your database credentials (as shown above).

4. Build the Project
Use Maven to build the project and resolve dependencies:
mvn clean install

5. Run the Application
Run the Spring Boot application:
mvn spring-boot:run

Alternatively, in an IDE:

Open the project in IntelliJ IDEA or Eclipse.
Locate the main class (e.g., EcommerceApplication.java).
Right-click and select Run.

6. Access the Application
Open your browser and navigate to:
http://localhost:8080


Register or log in as a customer (USER) or admin (ADMIN).
Explore features like browsing products, adding to cart, and managing orders.

Project Structure

src/main/java/: Java source code (controllers, services, entities, repositories).
src/main/resources/: Configuration files (application.properties) and Thymeleaf templates (templates/).
src/main/resources/static/: Static resources (CSS, JavaScript).
pom.xml: Maven configuration file for dependencies and build settings.
target/: Generated after building (contains compiled classes and JAR file).

Deployment

Deploy the application to a cloud platform like Heroku:
Install the Heroku CLI.
Log in to Heroku: heroku login.
Create a new Heroku app: heroku create.
Add a Procfile in the root directory with:web: java -jar target/e-commerce-web-app-0.0.1-SNAPSHOT.jar


Configure environment variables for the database on Heroku.
Push to Heroku: git push heroku main.


Alternatively, deploy to AWS or Azure following their respective guides.

Error Handling

Backend: Custom exceptions and @ControllerAdvice for global error handling.
Frontend: Thymeleaf templates display user-friendly error messages (e.g., "Product not found").
Validation: Server-side validation with Spring’s @Valid and error messages shown on forms.

Contributing
Contributions are welcome! To contribute:

Fork this repository.
Create a new branch (git checkout -b feature-branch).
Make your changes and commit (git commit -m "Add feature").
Push to your fork (git push origin feature-branch).
Open a pull request.

License
This project is licensed under the MIT License.
Submission

The source code and documentation are hosted publicly on GitHub.
The repository link has been submitted via Google Classroom as per the instructions.

