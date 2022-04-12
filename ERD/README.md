# DBMS
Database management system is software that is used to manage the database.

## What is Database

The database is a collection of inter-related data which is used to retrieve, insert and delete the data efficiently. It is also used to organize the data in the form of a table, schema, views, and reports, etc.

## Database Management System

* Database management system is a software which is used to manage the database. For example: MySQL, Oracle, etc are a very popular commercial database which is used in different applications.

* DBMS provides an interface to perform various operations like database creation, storing data in it, updating data, creating a table in the database and a lot more.

* It provides protection and security to the database. In the case of multiple users, it also maintains data consistency.

## Characteristics of DBMS
1. It uses a digital repository established on a server to store and manage the information.
2. It can provide a clear and logical view of the process that manipulates data.
3. DBMS contains automatic backup and recovery procedures.
4. It contains ACID properties which maintain data in a healthy state in case of failure.
5. It can reduce the complex relationship between data.
6. It is used to support manipulation and processing of data.
7. It is used to provide security of data.
8. It can view the database from different viewpoints according to the requirements of the user.

## Advantages of DBMS
1. **Controls database redundancy**: It can control data redundancy because it stores all the data in one single database file and that recorded data is placed in the database.
2. **Data sharing**: In DBMS, the authorized users of an organization can share the data among multiple users.
3. **Easily Maintenance**: It can be easily maintainable due to the centralized nature of the database system.
4. **Reduce time**: It reduces development time and maintenance need.
5. **Backup**: It provides backup and recovery subsystems which create automatic backup of data from hardware and software failures and restores the data if required.
6. **multiple user interface**: It provides different types of user interfaces like graphical user interfaces, application program interfaces

## Disadvantages of DBMS
1. **Cost of Hardware and Software**: It requires a high speed of data processor and large memory size to run DBMS software.
2. **Size**: It occupies a large space of disks and large memory to run them efficiently.
3. **Complexity**: Database system creates additional complexity and requirements.
4. **Higher impact of failure**: Failure is highly impacted the database because in most of the organization, all the data stored in a single database and if the database is damaged due to electric failure or database corruption then the data may be lost forever.

# Database Schema
A database schema is the skeleton structure that represents the logical view of the entire database. It defines how the data is organized and how the relations among them are associated.

## Database Schema categories :
1. **Physical Database Schema** − This schema pertains to the actual storage of data and its form of storage like files, indices, etc. It defines how the data will be stored in a secondary storage.

2. **Logical Database Schema** − This schema defines all the logical constraints that need to be applied on the data stored. It defines tables, views, and integrity constraints.

# Keys
Keys play an important role in the relational database.
It is used to uniquely identify any record or row of data from the table. It is also used to establish and identify relationships between tables.

## Types of keys:
1. Primary key : It is the first key used to identify one and only one instance of an entity uniquely.
2. Candidate key : A candidate key is an attribute or set of attributes that can uniquely identify a tuple.
3. Super Key : Super key is an attribute set that can uniquely identify a tuple. A super key is a superset of a candidate key.
4. Foreign keys : they are the column of the table used to point to the primary key of another table.
5. Alternate key
6. Composite key
7. Artificial key

***To learn more*** (https://www.javatpoint.com/dbms-tutorial)