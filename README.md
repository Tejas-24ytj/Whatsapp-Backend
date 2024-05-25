# WhatsApp Backend in Spring Boot

This project implements a backend for a WhatsApp-like messaging application using Spring Boot. It provides APIs for user authentication, messaging, and chat management.

## Features

- **User Authentication**: Register and login functionality with JWT-based authentication.
- **Messaging**: Real-time messaging between users.
- **Chat Management**: Create, join, and manage group chats.
- **User Profiles**: Update and view user profiles.

## Technologies Used

- **Spring Boot**: Backend framework.
- **Spring Security**: For authentication and authorization.
- **JWT (JSON Web Tokens)**: For securing endpoints.
- **Spring Data JPA**: For data persistence.
- **H2 Database**: In-memory database for development and testing.
- **WebSocket**: For real-time communication.
- **Lombok**: To reduce boilerplate code.
- **Maven**: Build tool.

## Getting Started

### Prerequisites

- Java 11 or higher
- Maven 3.6.0 or higher

### Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/whatsapp-backend-springboot.git
    cd whatsapp-backend-springboot
    ```

2. **Build the project**:
    ```bash
    mvn clean install
    ```

3. **Run the application**:
    ```bash
    mvn spring-boot:run
    ```

### Configuration

The application configuration is handled via the `application.properties` file located in the `src/main/resources` directory. Here, you can configure database connection properties, JWT secret key, and other settings.

Example `application.properties`:

```properties
# Server configuration
server.port=8080

# H2 Database configuration
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=password
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.h2.console.enabled=true

# JWT Configuration
jwt.secret=your_secret_key
jwt.expirationMs=86400000
