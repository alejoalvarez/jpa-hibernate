# JPA - Hibernate

## JPA - (Java Persistence API)

JPA is a part of the EJB 3 specification (JSR 220). Therefore it does not really exist as a framework, but is simply a document.

A document that specifies the basic principles of persistence layer management in the Java EE world.

## Hibernate

Framework that manages the persistence layer through xml files or annotations.

<p align="center">
<img height="270" src="JPA-Hibernate">
</p>

## Relationship between JPA and Hibernate

The relationship between JPA and Hibernate is that the latter implements the JPA specification as part of its code. In other words, we can use Hibernate to build a persistence layer relying on the definitions and rules of the JPA specification, although it is not mandatory.

<p align="center">
<img height="270" src="relation-JPA-Hibernate">
</p>

Of course, this does not mean that Hibernate simply implements the JPA standard. Hibernate is much larger than the JPA specification and adds more functionality.

<p align="center">
<img height="270" src="Hibernate1">
</p>


## Hibernate and NoSQL

One of the features that Hibernate supports today is the ability to work with NoSQL databases, something that JPA does not cover. This support that Hibernate brings allows us to work with MongoDB type databases (oriented to documents). Now, as long as we use Hibernate directly and rely on the proprietary annotations that it uses to support this new type of database.

<p align="center">
<img height="270" src="hibernate-nosql">
</p>

