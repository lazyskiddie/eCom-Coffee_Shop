# Ember & Oak Coffee Shop

A classic-themed Java Spring Boot e-commerce website for a coffee shop brand, designed around a royal café aesthetic and a premium customer experience.

## Overview

Ember & Oak is a full-stack coffee shop storefront built with Java, Spring Boot, MySQL, JSP, and Spring Security. The application combines a storefront experience with an admin management panel so products and services can be managed efficiently.

The project is structured as a Spring MVC web application with JSP views and server-side rendering. It includes product browsing, cart checkout flows, image uploads, and access control for administrative actions.

## Tech Stack

- Java 17
- Spring Boot 4.1.0
- Spring Web MVC
- Spring Data JPA
- Spring Security
- MySQL
- JSP / JSTL
- Maven
- Tomcat embedded server

## Project Architecture

The application follows a standard Spring Boot MVC pattern:

- `com.example.E_commerce` — root package for the application
- `Admin` package — admin-specific services and repository code
- `ECommerceApplication` — Spring Boot startup class
- `MySecurityConfg` — security configuration and access control
- `adminConfiguratuion` — admin controller for CRUD operations
- `Coffee` and `AdminEntity` — model entities
- `application.properties` — database and MVC configuration
- `WEB-INF/view` — JSP pages for front-end rendering

## Key Features

### Customer-facing features
- Browse coffee and product offerings
- View product details
- Add products to cart
- Checkout flow
- Login and protected user access

### Admin features
- Admin dashboard
- Add new coffee/services
- Update existing service entries
- Delete products
- Upload associated product images

### Security
- Admin routes are protected with Spring Security
- Login page is configured for authenticated access
- Default admin user is created automatically on startup if not present

If your local database credentials differ, update the values in `application.properties` before running the app.

## Default Admin Credentials

On startup, the application checks whether an admin user exists and creates one automatically if missing.

- Username: `admin`
- Password: `admin123`

## Running the Project Locally

### Prerequisites

- Java 17+
- Maven
- MySQL server

### Run steps

1. Clone the repository:

```bash
git clone https://github.com/lazyskiddie/eCom-Coffee_Shop.git
cd eCom-Coffee_Shop
```

2. Create the MySQL database:

```sql
CREATE DATABASE database;
```

3. Update your database settings if necessary in `src/main/resources/application.properties`.

4. Launch the app:

```bash
./mvnw spring-boot:run
```

5. Access the app in a browser:

```text
http://localhost:8080
```

## Admin Access

The admin routes are protected and require login.

```text
Username: admin
Password: admin123
```

## Notes

- JSP pages are served from `src/main/webapp/WEB-INF/view`.
- Product images are uploaded into a local static resource path associated with the app.
- The project follows a warm, classic café visual identity inspired by a luxury royal theme.

## License

This project is licensed under the Apache License 2.0.

## Contributing

Contributions are welcome. Fork the project, create a feature branch, and submit a pull request with a clear summary of changes.

## Project Identity

Ember & Oak is a coffee shop e-commerce application focused on premium café culture, elegant presentation, and a simple but usable online shopping experience.
