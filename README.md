# SpringAngular

A Spring Boot web application that combines a secured Java backend with an AngularJS-based interface. The project includes user and role management, file upload and storage, patient-oriented views, REST endpoints, and image-processing support.

## Technology stack

- Java 8 and Spring Boot 2.0.5
- Spring MVC, Spring Security, Spring Data JPA, and Hibernate
- Oracle Database
- Thymeleaf and AngularJS
- Bootstrap and jQuery
- Deeplearning4j, ND4J, and DataVec
- Maven wrapper

## Project layout

```text
Server-Side/
├── pom.xml
├── src/main/java/project/assistant/
│   ├── Model/          # Persistence and view models
│   ├── Repositories/   # Spring Data repositories
│   ├── Services/       # Application and storage services
│   ├── MvcController/  # Server-rendered web routes
│   └── RestController/ # JSON/REST endpoints
├── src/main/resources/
│   ├── application.properties
│   └── static/         # JavaScript, CSS, images, and vendor assets
└── src/main/webapp/views/ # Login, home, and patient views
```

## Prerequisites

- JDK 8
- Oracle Database/XE with an application schema
- A Unix-like shell or Windows PowerShell/Command Prompt

## Configuration

The application currently reads its database and server configuration from:

```text
Server-Side/src/main/resources/application.properties
```

Update the Oracle URL, username, password, and driver settings for your environment. The default server port is `9090`. Before deploying the application, replace the example database credentials and move secrets to environment-specific configuration.

## Run locally

```bash
git clone https://github.com/omidrajabi6868/SpringAngular.git
cd SpringAngular/Server-Side
./mvnw spring-boot:run
```

On Windows, use:

```powershell
mvnw.cmd spring-boot:run
```

Then open [http://localhost:9090](http://localhost:9090).

## Build and test

```bash
cd Server-Side
./mvnw clean test
./mvnw clean package
```

The Maven build produces a WAR package. The repository also contains a `UserControllerTest` test class under `src/test`.

## Main capabilities

- Database-backed authentication and role lookup
- User, account, file, and patient controllers
- Multipart file uploads and per-user storage
- REST endpoints consumed by the AngularJS client
- English and Persian message resources
- Image and deep-learning libraries available to the server-side workflow

## Notes

This is an older Spring Boot/Java 8 application. Use versions compatible with the dependencies pinned in `pom.xml`, particularly Spring Security, Hibernate, Deeplearning4j, and ND4J.
