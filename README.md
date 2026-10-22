# Spring Boot Foundation

Personal knowledge base and practice project for learning Spring Boot fundamentals.

## Structure

```text
springboot-foundation/
│
├── concepts/
│   ├── spring-boot.md
│   ├── maven.md
│   ├── dependency-injection.md
│   ├── rest-api.md
│   ├── validation.md
│   ├── exception-handling.md
│   ├── logging.md
│   ├── profiles.md
│   └── testing.md
│
├── labs/
│   ├── spring-boot-lab.md
│   ├── dependency-injection-lab.md
│   └── ...
│
├── examples/
│   └── implementation examples
│
└── product-service/
    └── Spring Boot application
```

## How I Learn

For each topic:

1. Read the concept.
2. Complete the lab.
3. Implement it in the project.
4. Save useful examples.

Example:

```text
concepts/spring-boot.md
        ↓
labs/spring-boot-lab.md
        ↓
product-service/
        ↓
examples/
```

## Topics

### Foundation

- Spring Boot
- Maven

### Core Development

- Dependency Injection
- REST APIs
- Validation
- Exception Handling
- Logging

### Configuration

- Profiles

### Quality

- Testing

## Project

The practical application used throughout the repository.

Planned endpoints:

```text
GET /health
GET /products
POST /products
```

## Commands

Run application:

```bash
mvn spring-boot:run
```

Run tests:

```bash
mvn test
```

Build application:

```bash
mvn package
```

## Goal

By the end of this repository I should be able to:

- Understand Spring Boot fundamentals
- Build REST APIs
- Configure applications
- Use Dependency Injection
- Validate requests
- Handle exceptions
- Add logging
- Write tests
- Explain Spring Boot concepts confidently
