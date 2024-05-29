# Backend Coding Standards

Consistency in coding style and practices is essential for maintaining a clean and understandable codebase. These standards aim to establish guidelines for writing Java code in a Spring Boot backend.

## Spring boot
project structure the backend will use

```bash

└─ Backend
   ├─ src
   │  ├─ main
   │  │  ├─ java
   │  │  │  └─ com
   │  │  │     └─ back
   │  │  │        └─ demo
   │  │  │           ├─ controller
   │  │  │           │  └─ ExampleController.java
   │  │  │           ├─ model
   │  │  │           │  └─ ExampleModel.java
   │  │  │           ├─ repository
   │  │  │           │  └─ ExampleRepository.java
   │  │  │           ├─ service
   │  │  │           │   └─ ExampleService.java
   │  │  │           │
   │  │  │           ├─ BackendApplication.java
   │  │  │           └─ HealthCheckController.java  
   │  │  │ 
   │  │  └─ resources
   │  │     └─ application.properties
   │  │  
   │  └─ test
   │     └─ java
   │        └─ com
   │           └─ back
   │              └─ demo
   │                 ├─ controller
   │                 │   └─ ExampleControllerTest.java
   │                 │
   │                 └─ BackendApplicationTests.java
   │
   │ 
   └─ pom.xml


```
## Controllers

- Use `PascalCase` for controller class names.
- Use `camelCase` for method names within controllers.
- Controllers should be thin and delegate business logic to services.

**Example:** 

**Example:** 

```java
@RestController
@RequestMapping("/api")
public class ExampleController {

    @Autowired
    private ExampleService exampleService;

    @GetMapping("/example")
    public ResponseEntity<List<ExampleModel>> getAllExamples() {
        List<ExampleModel> examples = exampleService.getAllExamples();
        return ResponseEntity.ok(examples);
    }

    // Other controller methods...
}
```



## Models

- Use `PascalCase` for model class names.
- Models should represent entities or DTOs (Data Transfer Objects).
- Use appropriate annotations for persistence (e.g., JPA annotations for entities).

**Example:** 
```java
@Entity
@Table(name = "examples")
public class ExampleModel {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    private String name;

    // Getters and setters...
}

```

## Services

- Use `PascalCase` for service class names.
- Services should encapsulate business logic.
- Use `camelCase` for method names within services.

**Example:** 
```java
@Service
public class ExampleService {

    @Autowired
    private ExampleRepository exampleRepository;

    public List<ExampleModel> getAllExamples() {
        return exampleRepository.findAll();
    }

    // Other service methods...
}


```

## Repository


- Use `PascalCase` for repository class names.
- Repositories should extend JpaRepository or appropriate Spring Data repository interfaces.


**Example:** 
```java
@Repository
public interface ExampleRepository extends JpaRepository<ExampleModel, Long> {
    // Custom query methods...
}

```

## Exception Handling

- Use `@ControllerAdvice` for global exception handling.
- Define custom exception classes for specific error scenarios.

## Logging

- Use logging frameworks like SLF4J with Logback for logging.
- Log meaningful information at appropriate levels (e.g., DEBUG, INFO, ERROR).
- 
## Testing

- Write unit tests using JUnit and Mockito for service and repository layers.
- Use Spring Boot's @SpringBootTest for integration tests.
Aim for high test coverage to ensure code reliability

## Documentation
- Document APIs using Swagger or Spring REST Docs.
- Use JavaDoc comments for documenting classes, methods, and parameters.
- service contracts are REQUIRED to be documented.

These coding standards provide a foundation for maintaining a clean, readable, and maintainable Spring Boot Java backend codebase. Consistently applying these guidelines will contribute to the overall quality and scalability of the project.