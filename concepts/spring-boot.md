# Spring Boot

## Purpose

Spring Boot is a framework built on top of the Spring Framework that simplifies the development of Java applications.

It reduces the amount of configuration required to create production-ready applications and provides sensible defaults for common development needs.

---

# Why Spring Boot Exists

Traditional Spring applications often require extensive configuration before useful development can begin.

Spring Boot addresses this by:

- Automatically configuring common components
- Providing embedded application servers
- Offering starter dependencies
- Following convention-over-configuration principles
- Simplifying deployment and execution

The goal is to allow developers to focus on business logic rather than infrastructure setup.

---

# Core Concepts

## Spring Framework vs Spring Boot

The Spring Framework provides the core capabilities for enterprise Java development, including:

- Dependency Injection
- Bean Management
- Spring MVC
- Application Context

Spring Boot builds on these capabilities and reduces the amount of manual configuration required to use them.

In simple terms:

```text
Spring Framework = Foundation

Spring Boot = Foundation + Automation + Defaults
```

---

## Auto Configuration

Auto Configuration is one of Spring Boot's most important features.

When Spring Boot detects specific dependencies in a project, it automatically configures the required components.

For example:

```xml
spring-boot-starter-web
```

automatically enables:

- Spring MVC
- Jackson JSON serialization
- Embedded Tomcat
- HTTP request handling

Without Auto Configuration, these components would require manual setup.

---

## Starter Dependencies

Starter dependencies provide preconfigured groups of libraries for common use cases.

Example:

```xml
spring-boot-starter-web
```

includes everything typically required for web applications.

Benefits:

- Faster project setup
- Reduced dependency management
- Improved compatibility between libraries
- Consistent project structures

Common starters:

```text
spring-boot-starter-web
spring-boot-starter-test
spring-boot-starter-validation
spring-boot-starter-data-jpa
```

---

## Embedded Server

Spring Boot applications include an embedded web server.

Common choices:

- Tomcat (default)
- Jetty
- Undertow

Because the server is bundled with the application:

- No external server installation is required
- The application can run directly from the command line
- Deployment becomes simpler

Typical startup process:

```text
Application Starts
        ↓
Embedded Tomcat Starts
        ↓
Endpoints Become Available
```

---

## Convention Over Configuration

Spring Boot favors sensible defaults.

Instead of manually configuring every component, Spring Boot assumes common conventions.

Examples:

```text
application.properties
application.yml
src/main/java
src/test/java
```

These locations are automatically recognized without additional configuration.

This approach reduces boilerplate code and simplifies project setup.

---

## Application Entry Point

Every Spring Boot application starts from a class annotated with:

```java
@SpringBootApplication
```

Example:

```java
@SpringBootApplication
public class ProductServiceApplication {

    public static void main(String[] args) {
        SpringApplication.run(
            ProductServiceApplication.class,
            args
        );
    }
}
```

Responsibilities:

- Starts the Spring container
- Applies Auto Configuration
- Scans project components
- Boots the application

---

# Standard Project Structure

```text
src
├── main
│   ├── java
│   └── resources
│
└── test
```

## src/main/java

Contains application source code.

Examples:

```text
Controllers
Services
Repositories
Configuration Classes
```

---

## src/main/resources

Contains application resources.

Examples:

```text
application.properties
application.yml
Static Files
Templates
```

---

## src/test

Contains automated tests.

Examples:

```text
Unit Tests
Integration Tests
Controller Tests
```

---

## pom.xml

Maven configuration file.

Responsibilities:

- Dependency management
- Build configuration
- Plugin configuration
- Packaging instructions

---

# Configuration

Spring Boot automatically loads configuration from:

```text
application.properties
```

Example:

```properties
spring.application.name=product-service
server.port=8080
```

Common uses:

- Server configuration
- Database configuration
- Logging configuration
- Environment-specific settings

---

# Application Lifecycle

```text
Developer Runs Application
            ↓
SpringApplication.run()
            ↓
Spring Container Created
            ↓
Auto Configuration Applied
            ↓
Embedded Server Started
            ↓
Application Ready
```

---

# Benefits of Spring Boot

- Faster development
- Reduced configuration
- Embedded server support
- Production-ready features
- Consistent project structure
- Simplified dependency management
- Easy integration with the Spring ecosystem

---

# Common Beginner Mistakes

## Trying To Learn All Of Spring First

Spring Boot should be learned incrementally while building applications.

---

## Ignoring Project Structure

Understanding the project layout makes every future topic easier.

---

## Memorizing Annotations

Focus first on the problem each feature solves before learning annotations.

---

## Confusing Spring With Spring Boot

Spring Boot simplifies Spring but does not replace the Spring Framework.

---

# Key Takeaways

- Spring Boot is built on top of Spring Framework.
- Auto Configuration reduces manual setup.
- Starter dependencies simplify dependency management.
- Embedded servers remove the need for separate application servers.
- Convention over configuration reduces boilerplate code.
- Applications start from a class annotated with `@SpringBootApplication`.
- Configuration is commonly managed through `application.properties`.

---

# Interview Summary

Spring Boot is an opinionated framework built on top of the Spring Framework that simplifies Java application development through auto configuration, starter dependencies, embedded servers, and convention-over-configuration principles. It enables developers to build production-ready applications with minimal setup while focusing on business logic rather than infrastructure configuration.
