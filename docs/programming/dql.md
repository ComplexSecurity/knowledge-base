Doctrine Query Language (DQL) is a powerful query language used in the [Doctrine](../programming/doctrine.md) ORM ([Object-Relational Mapping](../programming/orp.md)) system for [PHP](../programming/php.md). DQL is designed to allow developers to interact with their database using a syntax that is similar to [SQL](../programming/sql.md) but is tailored for working with object-oriented entities rather than raw database tables.

DQL operates on the entities and their associations defined in the ORM mapping. Instead of dealing with database tables and columns directly, developers write queries in terms of their PHP entities and their relationships.

In DQL, entities are identified by their fully-qualified class names. This helps in navigating through associations and properties using the object-oriented syntax. While DQL has its unique syntax, it shares similarities with SQL, making it easier for developers familiar with SQL to transition. DQL queries often resemble SQL queries, but they are focused on working with objects and their associations.

DQL supports various types of joins and associations between entities, allowing developers to navigate through relationships and retrieve related data. DQL supports parameter binding, allowing developers to write parameterized queries. This helps prevent SQL injection and makes queries more flexible.

Like SQL, DQL supports aggregate functions (e.g., COUNT, MAX, MIN, AVG, SUM) for performing calculations on grouped data. A simple query may be:

```php
<?php
// DQL query to retrieve all users whose age is greater than 25
$dql = "SELECT u FROM User u WHERE u.age > :age";

// Create a Doctrine Query object
$query = $entityManager->createQuery($dql);

// Set a parameter value
$query->setParameter('age', 25);

// Execute the query and get the result
$users = $query->getResult();
```

In this example, `User` is a mapped entity, and the DQL query retrieves users whose age is greater than 25. The `:age` is a parameter that can be bound to a specific value when executing the query.
