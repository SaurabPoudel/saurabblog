+++
title = 'DBMS | Introduction'
date = 2024-07-04T22:04:05+05:45
draft = false
description=""
image ="/images/dbms1.jpg"
imageBig ="/images/dbms1.jpg"
categories= ["general","dbms"]
authors= ["Saurab Poudel"]
avatar = "/images/avatar.webp"
+++


## Concepts

- A database-management system (DBMS) is a collection of interrelated data and a set of programs to access those data.
- The collection of data, usually referred to as the database, contains information relevant to an enterprise.
- The primary goal of a DBMS is to provide a way to store and retrieve database information that is both convenient and efficient.
- Database systems are designed to manage large bodies of information.
-  Management of data involves defining structures for storage of information and providing mechanisms for the manipulation of information.
- Additionally, the database system must ensure the safety of the information stored, despite system crashes or attempts at unauthorized access.
- If data are to be shared among several users, the system must avoid possible anomalous results.
- Because information is so important in most organizations, computer scientists have developed a large body of concepts and techniques for managing data.

## Application

1. **Online Shopping**: E-commerce websites use DBMS to store customer information, order details, product catalogs, and payment transactions.
    
2. **Banking**: Banks use DBMS to manage customer accounts, transactions, and loan records.
    
3. **Healthcare**: Hospitals and medical institutions use DBMS to store patient records, medical histories, and treatment plans.
    
4. **Social Media**: Social media platforms like Facebook, Twitter, and Instagram use DBMS to store user profiles, posts, comments, and likes.
    
5. **Education**: Educational institutions use DBMS to manage student records, course schedules, and grades.
    
6. **Travel Booking**: Travel booking websites use DBMS to store flight schedules, hotel reservations, and customer information.
    
7. **Inventory Management**: Retail stores and warehouses use DBMS to track inventory levels, orders, and shipments.
    
8. **Customer Relationship Management (CRM)**: CRM systems like Salesforce use DBMS to manage customer interactions, sales data, and marketing campaigns.
    
9. **Supply Chain Management**: Companies use DBMS to manage supply chain operations, including inventory tracking, order fulfillment, and logistics.
    
10. **Government Services**: Government agencies use DBMS to manage citizen services, such as tax records, driver's licenses, and social security benefits.
    
11. **Financial Reporting**: Financial institutions use DBMS to generate financial reports, track investments, and analyze market trends.
    
12. **Research and Development**: Researchers use DBMS to store and analyze large datasets, including scientific data, surveys, and experiments.

## DBMS vs File System

**Data Redundancy**

- DBMS: Provides mechanisms to reduce data redundancy by storing redundant data in multiple locations or using techniques like data compression.
- File System: Does not provide built-in support for reducing data redundancy.

**Isolation**

- DBMS: Provides isolation between concurrent transactions, ensuring that each transaction sees a consistent view of the database.
- File System: Does not provide built-in support for isolation between concurrent file operations.

**Concurrency**

- DBMS: Supports concurrency control mechanisms to manage multiple users accessing and modifying data simultaneously.
- File System: Does not provide built-in support for concurrency control.

**Accessing**

- DBMS: Provides various access methods (e.g., SQL, NoSQL) to retrieve and manipulate data.
- File System: Provides file management commands (e.g., mkdir, rm, cp) to create, delete, and manipulate files.

**Integrity**

- DBMS: Ensures data integrity by enforcing constraints like primary keys, foreign keys, and check constraints.
- File System: Does not provide built-in support for ensuring data integrity.

**Atomicity**

- DBMS: Supports atomicity by treating multiple operations as a single unit of work, ensuring that either all or none of the operations are committed.
- File System: Does not provide built-in support for atomicity.

**Consistency**

- DBMS: Ensures consistency by maintaining a consistent view of the data across all transactions and users.
- File System: Does not provide built-in support for consistency.

**Security**

- DBMS: Provides various security mechanisms (e.g., user authentication, access control) to protect data from unauthorized access.
- File System: Provides basic file-level permissions and access controls, but does not provide the same level of security as a DBMS.

In summary, while both DBMS and File Systems are designed to store and manage data, they differ significantly in terms of their underlying architecture, functionality, and features.


**Objectives of Database Management System (DBMS)**

1. **Data Storage**: Store large amounts of data efficiently and effectively.
2. **Data Retrieval**: Provide a way to retrieve specific data quickly and easily.
3. **Data Manipulation**: Allow users to add, update, or delete data as needed.
4. **Data Integrity**: Ensure that the data is consistent and accurate by **enforcing constraints like primary keys, foreign keys, and check constraints**.
5. **Concurrent Access**: Support multiple users accessing and modifying data simultaneously without compromising data integrity.
6. **Security**: Protect data from unauthorized access, modification, or deletion.

**Evolution of Database Management System (DBMS)**

1. **Early Years (1960s-1970s)**: The first DBMS was developed in the 1960s, with early systems like IBM's Information Management System (IMS) and Digital Equipment Corporation's DECsystem-10.
2. **Relational Model (1970s-1980s)**: The relational model, introduced by Edgar F. Codd in 1970, revolutionized DBMS development. Relational databases like Oracle and Microsoft SQL Server became popular.
3. **Object-Oriented Model (1990s)**: Object-oriented programming (OOP) concepts were applied to DBMS development, leading to the creation of object-relational databases like Oracle's ODM and IBM's DB2.
4. **NoSQL Databases (2000s)**: The rise of big data and unstructured data led to the development of NoSQL databases like MongoDB, Cassandra, and HBase.
5. **Cloud Computing (2010s)**: Cloud computing enabled scalable and on-demand access to DBMS resources, leading to the growth of cloud-based databases like Amazon Aurora and Google Cloud SQL.
6. **Artificial Intelligence (AI) and Machine Learning (ML) Integration**: Modern DBMS are incorporating AI and ML capabilities to improve data analysis, prediction, and decision-making.

**Key Milestones**

1. 1970: Edgar F. Codd introduces the relational model.
2. 1980s: Relational databases like Oracle and Microsoft SQL Server become popular.
3. 1990s: Object-oriented programming concepts are applied to DBMS development.
4. 2000s: NoSQL databases emerge as a response to big data challenges.
5. 2010s: Cloud computing enables scalable access to DBMS resources.

**Current Trends**

1. **Cloud-Native Databases**: Cloud-based databases designed for scalability and on-demand access.
2. **Graph Databases**: Specialized databases for storing and querying graph data structures.
3. **Time-Series Databases**: Optimized databases for storing and analyzing large amounts of time-stamped data.
4. **AI-Driven Database Systems**: DBMS incorporating AI and ML capabilities to improve data analysis and decision-making.

The evolution of DBMS has been shaped by advances in technology, changing user needs, and the emergence of new data types and applications.

### **Data Abstraction**

Data abstraction is a fundamental concept in computer science that refers to the process of exposing only the essential features of data while hiding its internal implementation details. In other words, it's about presenting a simplified view of complex data structures or systems.

The goal of data abstraction is to:

1. **Hide Complexity**: Abstract away the internal implementation details of data structures or systems, making them easier to understand and work with.
2. **Focus on Essentials**: Expose only the essential features of data that are relevant to the user or application, while hiding unnecessary details.
3. **Improve Modularity**: Allow for modular design by separating the abstracted view from the underlying implementation.

Data abstraction is achieved through various techniques, including:

1. **Abstract Data Types (ADTs)**: Define a set of operations that can be performed on data without revealing its internal representation.
2. **Encapsulation**: Wrap complex data structures or systems within a layer of abstraction, making them easier to interact with.
3. **Interfaces**: Define a contract or interface that specifies how data should be accessed and manipulated, without exposing the underlying implementation.

### **Data Independence**

Data independence is a concept that refers to the ability of a database system to remain unaffected by changes in its underlying physical storage structure or hardware. In other words, it's about ensuring that the logical structure of the data remains unchanged despite changes in its physical representation.

The goal of data independence is to:

1. **Decouple Logical and Physical**: Separate the logical structure of the data from its physical representation, allowing for changes in one without affecting the other.
2. **Improve Flexibility**: Enable the database system to adapt to changing hardware or storage technologies without requiring significant modifications to the underlying data structures.

Data independence is achieved through various techniques, including:

1. **Logical Data Structures**: Define logical data structures that are independent of physical storage structures.
2. **View Mechanisms**: Use view mechanisms to present a logical view of the data that is decoupled from its physical representation.
3. **Query Optimization**: Optimize queries to minimize the impact of changes in physical storage or hardware on the logical structure of the data.

In summary, data abstraction and data independence are two fundamental concepts in computer science that enable us to design more modular, flexible, and maintainable database systems.


![[Pasted image 20240704093426.png]]


**Schema**

A schema is a blueprint or a conceptual representation of a database's structure, including its tables, relationships, and constraints. It defines the logical organization of data, including:

- Tables (or relations): The main components of a database that store related data.
- Attributes (or columns): The individual fields within each table that describe specific characteristics of the data.
- Relationships: The connections between tables, such as one-to-one, one-to-many, or many-to-many.

The schema serves as a template for creating and managing the physical database. It provides a high-level view of the database's structure, making it easier to understand and work with the data.

**Instances**

An instance is a specific realization of a schema, representing the actual data stored in the database. In other words, an instance is a concrete implementation of the schema, containing the actual values for each attribute (or column).

Think of it like a blueprint (schema) and a house built according to that blueprint (instance). The schema defines the structure of the house, while the instance represents the specific building with its unique characteristics.

For example:

- Schema: A customer database with tables for customers, orders, and products.
- Instance: A specific customer database containing actual data about John Smith's orders and product purchases.

In summary, a schema is a conceptual representation of a database's structure, while an instance is the actual data stored in the database, following the schema's guidelines.

## Concepts of DDL, DML and DCL

**DDL (Data Definition Language)**

DDL is a set of commands used to define the structure of a database, including:

* Creating tables, indexes, views, and other database objects
* Defining relationships between tables
* Specifying data types and constraints for each column

Examples of DDL statements include:

* `CREATE TABLE` to create a new table
* `ALTER TABLE` to modify an existing table's structure
* `DROP TABLE` to delete a table
* `CREATE INDEX` to create a new index on a table

DDL is used to define the schema of a database, which determines how data is organized and stored.

**DML (Data Manipulation Language)**

DML is a set of commands used to manipulate the data in a database, including:

* Inserting, updating, and deleting data
* Retrieving data using queries

Examples of DML statements include:

* `INSERT INTO` to add new data to a table
* `UPDATE` to modify existing data in a table
* `DELETE` to remove data from a table
* `SELECT` to retrieve data from one or more tables

DML is used to perform CRUD (Create, Read, Update, Delete) operations on the data stored in a database.

**DCL (Data Control Language)**

DCL is a set of commands used to control access to a database, including:

* Creating and managing user accounts
* Granting and revoking privileges for users or roles
* Setting permissions for specific actions or objects

Examples of DCL statements include:

* `CREATE USER` to create a new user account
* `GRANT` to grant privileges to a user or role
* `REVOKE` to revoke privileges from a user or role
* `SET ROLE` to set the current role for a user

DCL is used to manage access control and security in a database, ensuring that only authorized users can perform specific actions.

In summary:

* DDL defines the structure of a database (schema)
* DML manipulates the data stored in a database
* DCL controls access to a database and manages user privileges
