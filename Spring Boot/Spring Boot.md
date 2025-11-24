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
	- It also uses the autowire keyword for the repository DI - In case of 
-