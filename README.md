# JPA - Hibernate

- [EntityManager](https://github.com/alejoalvarez/JPA-Hibernate/blob/master/EntityManager.md)
- [@Entity](https://github.com/alejoalvarez/JPA-Hibernate/blob/master/Entity.md)
- [@Table](https://github.com/alejoalvarez/JPA-Hibernate/blob/master/Table.md)
- [@Id](https://github.com/alejoalvarez/JPA-Hibernate/blob/master/Id.md)
- [@IdClass](https://github.com/alejoalvarez/JPA-Hibernate/blob/master/IdClass.md)
- [hasCode and Equals](https://github.com/alejoalvarez/JPA-Hibernate/blob/master/HashCode-Equals.md)
- [@EmbeddedId](https://github.com/alejoalvarez/JPA-Hibernate/blob/master/EmbeddedId.md)
- [@Column](https://github.com/alejoalvarez/JPA-Hibernate/blob/master/Column.md)
- [@Enumerated](https://github.com/alejoalvarez/JPA-Hibernate/blob/master/Enumerated.md)
- [@Temporal](https://github.com/alejoalvarez/JPA-Hibernate/blob/master/Temporal.md)
- [@Lob](https://github.com/alejoalvarez/JPA-Hibernate/blob/master/Lob.md)
- [@Transient](https://github.com/alejoalvarez/JPA-Hibernate/blob/master/Transient.md)

## JPA - (Java Persistence API)

- JPA is a part of the EJB 3 specification (JSR 220). Therefore it does not really exist as a framework, but is simply a document.
- Document that specifies the basic principles of persistence layer management in the Java EE world.
In charge of converting the java objects into instructions for the database manager
- Java **standard proposal** to perform database **object** persistence (ORM)

**Advantages**
- It allows us to develop much faster
- Allows you to work with the database through Entities instead of queries
- It offers us a paradigm oriented 100% to Objects
- Eliminate runtime errors
- Improves software maintenance

**Disavantages**

- Does not offer native query functionality
- Performance is much lower than JDBC queries

## Hibernate

- Framework that manages the persistence layer through xml files or annotations.
- Hibernate is an Object-Relational Mapping (ORM) tool, that facilitates attribute mapping between a traditional relational database and an application's object model
- Is an ORM (the most popular implementing JPA)
- We can use Hibernate to build a persistence layer relying on the definitions and rules of the JPA specification, although it is not mandatory.

<p align="center">
<img height="300" src="https://github.com/alejoalvarez/JPA-Hibernate/blob/master/images/JPA-Hibernate.png">
</p>

## ORM (Obect Relational Mapping)

- The most important characteristic of an ORM is to be able to have the ability and the logic to convert a class with attributes and methods to tuples in the database.
- We do not have to worry about the database engine, since if we use the ORM capabilities correctly we can migrate quickly and transparently

## How to works Hibernate?

<p align="center">
<img height="300" src="https://github.com/alejoalvarez/JPA-Hibernate/blob/master/images/hibernate2.png">
</p>


**Objects inside Hibernate**

<p align="center">
<img height="400" src="https://github.com/alejoalvarez/JPA-Hibernate/blob/master/images/Hibernate3.png">
</p>

- **Hibernate Configuration Object**: The configuration object is the first Hibernate object and is generally created only once during application initialization. Represents a required properties or configuration file and provides two key components:
    - Database connection
    - Class Mapping Settings

- **SessionFactory target**: Configuration object is used to create a SessionFactory object for the application that uses the supplied configuration file, and allows a Session object to be executed.
- **Session object**: It is used to obtain a physical connection with a database. Session objects should not be kept open for long as they are typically not thread safe and should be created and destroyed as needed.
- **Transaction object**: This is an optional object and Hibernate applications can choose not to use this interface, instead managing transactions in their own application code.
- **Query Object**: Query objects use SQL or Hibernate Query Language (HQL) string to retrieve data from the database and create objects. A query instance is used to bind the query parameters, limit the number of results returned by the query, and finally, to execute the query.
- **Criteria object**: Criteria objects are used to create and run object queries and retrieve objects

## Relationship between JPA and Hibernate

The relationship between JPA and Hibernate is that the latter implements the JPA specification as part of its code. In other words, we can use Hibernate to build a persistence layer relying on the definitions and rules of the JPA specification, although it is not mandatory.

<p align="center">
<img height="300" src="https://github.com/alejoalvarez/JPA-Hibernate/blob/master/images/relation-JPA-Hibernate.png">
</p>

Of course, this does not mean that Hibernate simply implements the JPA standard. Hibernate is much larger than the JPA specification and adds more functionality.

<p align="center">
<img height="300" src="https://github.com/alejoalvarez/JPA-Hibernate/blob/master/images/Hibernate1.png">
</p>

## Hibernate and NoSQL

One of the features that Hibernate supports today is the ability to work with NoSQL databases, something that JPA does not cover. This support that Hibernate brings allows us to work with MongoDB type databases (oriented to documents). Now, as long as we use Hibernate directly and rely on the proprietary annotations that it uses to support this new type of database.

<p align="center">
<img height="300" src="https://github.com/alejoalvarez/JPA-Hibernate/blob/master/images/hibernate-nosql.png">
</p>

## JDBC

**Advantages**

- It offers superior performance since it is the most direct way of sending instructions to the database.
- It allows to fully exploit the functionalities of the database.

**Disadvantages**

- Maintenance is much more expensive.
- It introduces a lot of errors at runtime.
- Development is much slower.