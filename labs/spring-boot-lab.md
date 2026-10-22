# Spring Boot Lab

## Goal

Verify the main Spring Boot concepts using a real application.

---

# Exercise 1: Generate a Spring Boot Project

Go to:

https://start.spring.io

Configuration:

- Maven
- Java
- Spring Boot Latest Stable
- Java 17 or 21

Dependencies:

- Spring Web
- Validation
- DevTools
- Actuator
- Lombok
- Starter Test

Generate and open the project.

---

# Exercise 2: Explore the Project Structure

Locate:

- pom.xml
- src/main/java
- src/main/resources
- src/test

Questions to answer:

- What belongs in each folder?
- Which file controls dependencies?
- Which file controls configuration?

---

# Exercise 3: Run the Application

Run:

```bash
mvn spring-boot:run
```

Observe:

- Application starts successfully
- Startup logs appear
- Port used by the application

Learning objective:

Understand the Spring Boot startup process.

---

# Exercise 4: Verify Embedded Tomcat

Search startup logs for:

```text
Tomcat started on port(s)
```

Learning objective:

Confirm the application includes its own server.

---

# Exercise 5: Verify Configuration Loading

Open:

```text
application.properties
```

Add:

```properties
server.port=8081
```

Restart.

Verify:

```text
http://localhost:8081
```

Learning objective:

Understand how Spring Boot loads configuration.

---

# Exercise 6: Explore Starter Dependencies

Open:

```text
pom.xml
```

Locate:

```xml
spring-boot-starter-web
```

Inspect dependency tree.

Identify:

- Spring MVC
- Jackson
- Tomcat

Learning objective:

Understand the purpose of starter dependencies.

---

# Exercise 7: Locate the Entry Point

Find:

```java
@SpringBootApplication
```

Analyze:

```java
SpringApplication.run(...)
```

Learning objective:

Understand how Spring Boot starts.

---

# Success Criteria

You should be able to explain:

- What Spring Boot is
- Why Spring Boot exists
- What Auto Configuration does
- What Starter Dependencies are
- Why Tomcat starts automatically
- What application.properties does
- What pom.xml does
- What @SpringBootApplication does
- How a Spring Boot application starts
