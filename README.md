# Xindus Wishlist Management Project
This backend application serves as the backend solution for managing wishlists in an e-commerce platform. The application is built using Spring Boot, Spring Security with JWT authentication, and Spring Data JPA.

## Features
- User Authentication using Spring Security with JWT authentication.
- Wishlist Management for managing user wishlists, including creation and deletion of wishlist items.
- Database Integration with a relational database using Spring Data JPA for storing user information and wishlist items.

## Setup and Usage

## Prerequisites
- Java Development Kit (JDK) version 8 or higher
- Maven
 
### Install
Step1:- Clone the repository to your local machine:
- git clone https://github.com/narry581/XindusAssignment.git

Step2:- cd XindusAssignment

Step3:- mvn clean install

## Configuration

- Open the src/main/resources/application.properties file.
- Configure your database connection settings:
  - spring.datasource.url=jdbc:mysql://localhost:3306/wishlistmanagement
  - spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
  - spring.datasource.username=root
  - spring.datasource.password=7382612798
  
Step2:- Spring Security Configuration:
- Customize security settings, such as JWT token expiration time and secret key, in the SecurityConfig.java file.

### Run the Application
1. - mvn spring-boot:run

2. The application will start on the default port 8080.

### API Usage
1. Sign Up:
- Open Postman or any HTTP client application.
- Send a POST request to http://localhost:8080/api/addUser with JSON body containing user details:
  - {
    - "firstName": "firstname",
    - "lastName": "lastname",
    - "email": "email",
    - "password": "password"
  - }

2. Login:
- Send a POST request to http://localhost:8080/auth/login with JSON body containing user credentials:
  - {
    - "email": "example_email",
    - "password": "example_password"
   - }

## Note: Save the JWT token received in the response.

3. Accessing Other APIs:
- To access other APIs requiring authentication, include the JWT token in the Authorization header of your requests:
   - In Postman, set the Authorization type to "Bearer Token" and paste the JWT token obtained during login.
   - Use the following endpoints for other API functionalities:
     - Wishlist Management: http://localhost:8080/api/wishlists
     - Products: http://localhost:8080/api/products

 We hope this documentation has a clear guidance on setting up, configuring, and running the application.
Thank you
