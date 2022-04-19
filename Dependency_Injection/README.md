
# Dependency Injection
 Dependency Injection is an implementation of "Inversion of Control". Inversion of Control (IoC) says that the objects do not create other objects on which they rely to do their work.

## Implementation
[Dependency Injection](https://www.c-sharpcorner.com/article/dependency-injection-in-asp-net-mvc-5/)

# Repository Pattern
  the Repository Design Pattern in C# mediates between the domain and the data mapping layers using a collection-like interface for accessing the domain objects. Repository Design Pattern separates the data access logic and maps it to the entities in the business logic. It works with the domain entities and performs data access logic.

  ## Advantages of Repository Design Pattern
* Testing controllers becomes easy because the testing framework need not run against the actual database access code.
* Repository Design Pattern separates the actual database, queries and other data access logic from the rest of the application.
* Business logic can access the data object without having knowledge of the underlying data access architecture.
* Business logic is not aware of whether the application is using LINQ to SQL or ADO.NET. In the future, underlying data sources or architecture can be changed without affecting the business logic.
* Caching strategy for the data source can be centralized.
* Centralizing the data access logic, so code maintainability is easier

## Implementation
[Repository Pattern implementation](https://www.c-sharpcorner.com/article/repository-design-pattern-in-asp-net-mvc/)

# SOLID
SOLID design principles in C# are basic design principles. SOLID stands for Single Responsibility Principle (SRP), Open closed Principle (OSP), Liskov substitution Principle (LSP), Interface Segregation Principle (ISP), and Dependency Inversion Principle (DIP).  

## SOLID principles
**S: Single Responsibility Principle (SRP)**
The Single Responsibility Principle gives us a good way of identifying classes at the design phase of an application and it makes you think of all the ways a class can change.

SRP says "Every software module should have only one reason to change".

**O: Open/Closed Principle**
The Open/closed Principle says "A software module/class is open for extension and closed for modification".
- "Closed for modification" means we have already developed a class and it has gone through unit testing.

**L: Liskov Substitution Principle**
The Liskov Substitution Principle (LSP) states that "you should be able to use any derived class instead of a parent class and have it behave in the same manner without modification". It ensures that a derived class does not affect the behavior of the parent class, in other words,, that a derived class must be substitutable for its base class.

**I: Interface Segregation Principle (ISP)**
The Interface Segregation Principle states "that clients should not be forced to implement interfaces they don't use. Instead of one fat interface, many small interfaces are preferred based on groups of methods, each one serving one submodule.".

An interface should be more closely related to the code that uses it than code that implements it. So the methods on the interface are defined by which methods the client code needs rather than which methods the class implements. So clients should not be forced to depend upon interfaces that they don't use.

**D: Dependency Inversion Principle**
The Dependency Inversion Principle (DIP) states that high-level modules/classes should not depend on low-level modules/classes. Both should depend upon abstractions. Secondly, abstractions should not depend upon details. Details should depend upon abstractions.

High-level modules/classes implement business rules or logic in a system (application). Low-level modules/classes deal with more detailed operations.

***To learn more*** [SOLID](https://www.c-sharpcorner.com/UploadFile/damubetha/solid-principles-in-C-Sharp/)
