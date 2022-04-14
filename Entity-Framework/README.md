# Entity Framework Core and APIs

## What is Entity Framework

Entity Framework is an open-source ORM (Object Relational Mapping) Framework for the .NET applications supported by Microsoft. It enables the developers to work with the data using the objects of domain-specific classes without focussing on the database tables and columns where the data is stored.

## What is an Entity in Entity Framework

An entity in Entity Framework is a class that maps to a database table. This class must be included as a DbSet type property in the DbContext class. Entity Framework API maps each entity to a table and each property of an entity to a column in the database.

## Entity Framework Architecture
**EDM (Entity Data Model)**: EDM consists of three parts. These three parts are:
Conceptual Model, Mapping, and Storage Model.

**Conceptual Model**: The conceptual model contains the modal classes and their relationships. The conceptual model is independent of the database design table.

**Storage Model**: The storage model is the database design model which includes tables, views, stored procedure, their relationships, and keys.

**Mapping**: Mapping consists the information about how the conceptual model is mapped to the storage model.

**LINQ-to-Entities**: LINQ-to-Entities (L2E) is a query language that is used to write queries against the model of the object. It returns the entities, which is defined in the conceptual model. We can use our LINQ-to-SQL skills here.

**Entity SQL**: Entity SQL is another query language (for EF 6 only), just like LINQ to Entities. 

**Object Service**: Object Service is the main entry point for accessing the data from the database and return it. Object Service is responsible for materialization, and materialization is the process of converting the data returned from an entity client data provider to an entry object structure.

**Entity Client Data Provider**: The main responsibility of this layer is to convert the LINQ-to-Entities or Entity SQL Queries into a SQL Query, which is understood by the database. It communicates with the ADO.NET data provider, which in turn sends or retrieves the data from the database.

**ADO.NET Data Provider**: This layer communicates with the database using the Standard ADO.Net.

***To learn more*** [Entity Framework](https://www.javatpoint.com/entity-framework)