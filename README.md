# Project Guide: Java Spring Boot

This document provides instructions for setting up, running, and developing the Java Spring Boot application.

## 1. Project Overview

This is a Java Spring Boot project. The main application entry point can be found in `src/main/java/.../UstaadApplication.java`.

## 2. Prerequisites

Before you begin, ensure you have the following installed:

*   **Java Development Kit (JDK):** Version 21 or higher (based on common Spring Boot practices and project `pom.xml` might specify a version).
*   **Apache Maven:** For building and dependency management.
*   **Git:** For version control.
*   **IDE:** An IDE like IntelliJ IDEA or VS Code with Java extensions is recommended.

## 3. Getting Started

### 3.1. Clone the Repository

If you haven't already, clone the project repository:

```bash
git clone https://github.com/pandeyGanesh/ustaad.git
cd ustaad
```

### 3.2. Build the Project

Navigate to the project's root directory (where `pom.xml` is located) and build the project using Maven:

```bash
mvn clean install
```
This command compiles the code, runs tests, and packages the application into a JAR file.

## 4. Running the Application

### 4.1. From JAR file

After building, you can run the Spring Boot application using the generated JAR file:

```bash
java -jar target/ustaad-0.0.1-SNAPSHOT.jar # Adjust JAR name if different
```

### 4.2. From Maven

You can also run the application directly via Maven Spring Boot plugin:

```bash
mvn spring-boot:run
```

## 5. Development

### 5.1. Common Maven Commands

*   **Clean build:** `mvn clean install`
*   **Run tests:** `mvn test`
*   **Skip tests during build:** `mvn clean install -DskipTests`
*   **Generate IDE project files (for IntelliJ - generally not needed as IntelliJ handles `pom.xml` directly):** `mvn idea:idea`

### 5.2. Configuration

Application configuration is typically managed in `src/main/resources/application.properties` (or `application.yml`).

### 5.3. Adding Dependencies

To add new dependencies, edit the `pom.xml` file and add the `<dependency>` entry within the `<dependencies>` section. After adding, run `mvn clean install` to download and integrate the new dependencies.

## 6. Testing

Tests are located in `src/test/java/com/pandeyxyz/ustaad/`.
To run all tests:

```bash
mvn test
```

## 7. Deployment

Deployment instructions will depend on your target environment (e.g., Docker, Kubernetes, Cloud Provider). Specific instructions should be added here as the project matures.

*We are leveraging AI agents, including Gemini CLI, to assist in the development of this project. This approach helps us enhance efficiency and explore innovative development methodologies.*