- Controller 
- Service  - It has 2 parts Implementation and Interface
- Repository 
- Entity

Entity : Object which relates to a table
- @Table, @Entity, @Getter, @Setter, NoArgsConstructor, @AllArgsConstructor
- @Id, @GeneratedValue, @Column

Repository 
 - This class extends the JPARepository - it takes to values - Entityname and Id

Service 
- Interface - it defines the methods to be implemented - takes DTO object and returns DTO object
- Implementation - 
	- It implements the methods defined in the interface
	- It also uses the autowired keyword for the repository DI - In case of constructor injection it is not required
	- It has DTO as an input to the methods and output is also a DTO

Mapper class
- It has methods to convert the DTO object to Entity object and vis-e-versa

Controller : 
- RestController as an annotation on the class,
- RequestMapping to map the request to the controller
- Methods - Get, Post, Put, Patch, Delete
- Eg- Post method returns a ResponseEntity<'Of DTO Type'>
- PostMapping - on the method
- RequestBody - convert the request body mostly json to the object - json -> to java
- Path variable - identify resource as a part of the url, uses {} to enclose the
- RequestParam - they act as filters
- ![[Pasted image 20251125193548.png]]-
- RequestBody - for body from json, take request body as Map<> and then extract the parameter for which you want to get the request body
  
  Spring Boot uses various annotations to simplify configuration and development, which can be categorized by their function. 

Core Configuration and Component Management

These annotations are essential for bootstrapping the application, defining components (beans), and enabling core functionality. 

- **`@SpringBootApplication`**: Marks the main class of a Spring Boot application, combining `@Configuration`, `@EnableAutoConfiguration`, and `@ComponentScan` into one convenient annotation.
- **`@Configuration`**: Indicates that a class is a source of bean definitions for the Spring application context.
- **`@EnableAutoConfiguration`**: Tells Spring Boot to automatically configure the application based on the dependencies present in the classpath, significantly reducing manual configuration.
- **`@ComponentScan`**: Configures which packages the Spring container should scan to find and register components annotated with `@Component`, `@Service`, `@Repository`, or `@Controller`.
- **`@Component`**: A generic stereotype for any Spring-managed component.
- **`@Service`**: A specialization of `@Component` used for classes in the service layer, typically holding business logic.
- **`@Repository`**: A specialization of `@Component` for Data Access Objects (DAOs) and repository classes, providing automatic exception translation from database-specific exceptions.
- **`@Bean`**: Used on a method within a `@Configuration` class to indicate that the method's return value should be registered as a Spring-managed bean. 

Dependency Injection and Value Injection 

These annotations facilitate the wiring of dependencies and external property values. 

- **`@Autowired`**: Automatically injects dependent beans into fields, constructors, or setter methods. Constructor injection is generally considered a best practice.
- **`@Qualifier`**: Used with `@Autowired` to specify exactly which bean to inject when multiple beans of the same type exist.
- **`@Value`**: Injects values into fields from properties files (e.g., `application.properties`), environment variables, or system properties. 

Web Layer and Request Handling

These annotations are crucial for building RESTful APIs and handling HTTP requests. 

- **`@Controller`**: Marks a class as a Spring MVC controller, typically used in applications that render views (e.g., HTML).
- **`@RestController`**: A convenience annotation that combines `@Controller` and `@ResponseBody` for building RESTful web services that return data (like JSON or XML) directly in the response body.
- **`@RequestMapping`**: Maps web requests to specific handler methods or classes. It can specify the HTTP method (GET, POST, etc.).
- **`@GetMapping`**, **`@PostMapping`**, **`@PutMapping`**, **`@DeleteMapping`**: Specialized, more explicit versions of `@RequestMapping` for handling specific HTTP verbs.
- **`@PathVariable`**: Binds a method parameter to a URI template variable (e.g., extracting an `id` from `/users/{id}`).
- **`@RequestParam`**: Binds a method parameter to a web request query parameter (e.g., extracting `keyword` from `/search?keyword=laptop`).
- **`@RequestBody`**: Binds the body of an HTTP request to a method parameter, automatically converting JSON or XML into a Java object. 

Data Persistence and Transactions

These annotations are used in the data access layer to manage data and transactions. 

- **`@Entity`**: Marks a class as a JPA entity, meaning it corresponds to a table in a database.
- **`@Id`**: Specifies the primary key of an entity.
- **`@GeneratedValue`**: Specifies how the primary key value should be generated.
- **`@Transactional`**: Ensures that a method or class is executed within a transactional context, automatically handling commit or rollback operations.