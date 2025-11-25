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