# Types of Databases

[![N|Solid](https://static.javatpoint.com/dbms/images/types-of-databases.png)](https://www.javatpoint.com/types-of-databases)

## 1. Relational databases
The name comes from the way that data is stored in multiple, related tables. Within the tables, data is stored in rows and columns. The relational database management system (RDBMS) is the program that allows you to create, update, and administer a relational database. Structured Query Language (SQL) is the most common language for reading, creating, updating and deleting data. Relational databases are very reliable. They are compliant with ACID (Atomicity, Consistency, Isolation, Durability), which is a standard set of properties for reliable database transactions. Relational databases work well with structured data. Organizations that have a lot of unstructured or semi-structured data should not be considering a relational database.

**Examples:**  Microsoft SQL Server, Oracle Database, MySQL, PostgreSQL, IBM Db2

## 2. NoSQL databases
NoSQL is a broad category that includes any database that doesn’t use SQL as its primary data access language. These types of databases are also sometimes referred to as non-relational databases. Unlike in relational databases, data in a NoSQL database doesn’t have to conform to a pre-defined schema, so these types of databases are great for organizations seeking to store unstructured or semi-structured data. One advantage of NoSQL databases is that developers can make changes to the database on the fly, without affecting applications that are using the database.


**Examples:**  Apache Cassandra, MongoDB, CouchDB, and CouchBase


## 3. Cloud databases
A cloud database refers to any database that’s designed to run in the cloud. Like other cloud-based applications, cloud databases offer flexibility and scalability, along with high availability. Cloud databases are also often low-maintenance, since many are offered via a SaaS model.

**Examples:**  Microsoft Azure SQL Database, Amazon Relational Database Service, Oracle Autonomous Database


## 4. Columnar databases
Also referred to as column data stores, columnar databases store data in columns rather than rows. These types of databases are often used in data warehouses because they’re great at handling analytical queries. When you’re querying a columnar database, it essentially ignores all of the data that doesn’t apply to the query, because you can retrieve the information from only the columns you want.

**Examples:**  Google BigQuery, Cassandra, HBase, MariaDB, Azure SQL Data Warehouse


## 5. Wide column databases
Wide column databases, also known as wide column stores, are schema-agnostic. Data is stored in column families, rather than in rows and columns. Highly scalable, wide column databases can handle petabytes of data, making them ideal for supporting real-time big data applications.

**Examples:**  BigTable, Apache Cassandra and Scylla


## 6. Object-oriented databases

An object-oriented database is based on object-oriented programming, so data and all of its attributes, are tied together as an object. Object-oriented databases are managed by object-oriented database management systems (OODBMS). These databases work well with object-oriented programming languages, such as C++ and Java. Like relational databases, object-oriented databases conform to ACID standards.

 

**Examples:** Wakanda, ObjectStore

## 7. Key-value databases

One of the simplest types of NoSQL databases, key-value databases save data as a group of key-value pairs made up of two data items each. They’re also sometimes referred to as a key-value store. Key-value databases are highly scalable and can handle high volumes of traffic, making them ideal for processes such as session management for web applications, user sessions for massive multi-player online games, and online shopping carts.

 

**Examples:** Amazon DynamoDB, Redis

 
## 8. Hierarchical databases

Hierarchical databases use a parent-child model to store data. If you were to draw a picture of a hierarchical database, it would look like a family tree, with one object on top branching down to multiple objects beneath it. The one-to-many format is rigid, so child records can’t have more than one parent record. Originally developed by IBM in the early 1960s, hierarchical databases are commonly used to support high-performance and high availability applications.

 

**Examples:** IBM Information Management System (IMS), Windows Registry

 
## 9. Document databases

Document databases, also known as document stores, use JSON-like documents to model data instead of rows and columns. Sometimes referred to as document-oriented databases, document databases are designed to store and manage document-oriented information, also referred to as semi-structured data. Document databases are simple and scalable, making them useful for mobile apps that need fast iterations.

**Examples:** MongoDB, Amazon DocumentDB, Apache CouchDB

 
## 10. Graph databases

Graph databases are a type of NoSQL database that are based on graph theory. Graph-Oriented Database Management Systems (DBMS) software is designed to identify and work with the connections between data points. Therefore graph databases are often used to analyze the relationships between heterogeneous data points, such as in fraud prevention or for mining data about customers from social media.

 

**Examples:** Datastax Enterprise Graph, Neo4J

 
## 11. Time series databases

A time series database is a database optimized for time-stamped, or time series, data. Examples of this type of data include network data, sensor data, and application performance monitoring data. All of those Internet of Things sensors that are getting attached to everything put out a constant stream of time series data.

 

**Examples:** Druid, eXtremeDB, InfluxDB






**source:** https://www.matillion.com/blog/the-types-of-databases-with-examples














