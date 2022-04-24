# DTO (Data Transfer objects)

## What Is a DTO?
A DTO (Data Transfer Object) is an object that defines how data will be sent between applications.

It’s used only to send and receive data and does not contain in itself any business logic.

## Why Use DTOs?
The use of DTOs is very common in web development with ASP.NET Core as they provide solutions for many needs. Below are some of them:

* Separate the service layer from the database layer
* Hide specific properties that clients don’t need to receive
* Omit properties to reduce the payload size
* Manipulate nested objects to make them more convenient for clients
* Avoid “overpost” vulnerabilities

DTOs provide an efficient way to separate domain objects from the presentation layer. This way, you can change the presentation layer without affecting the existing domain layers, and vice versa.

## Use DTOs for abstraction
You can take advantage of DTOs to abstract the domain objects of your application from the user interface or the presentation layer. In doing so, the presentation layer of your application is decoupled from the service layer.

## DTO serialization challenges
You should be able to serialize/deserialize a DTO seamlessly so that it can be passed down the wire. In practice, however, you might have to solve some serialization problems when working with DTOs. You might have several entities or model classes in a real-world application and each of them may hold references to each other.

***To learn more***[DTO](https://www.telerik.com/blogs/dotnet-basics-dto-data-transfer-object)
