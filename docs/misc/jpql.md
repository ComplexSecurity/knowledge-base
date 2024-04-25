Java Persistence Query Language (JPQL) is a query language used in the [[Java Persistence API (JPA)]] for making queries against entities stored in a relational database. JPQL is an object-oriented query language, similar in nature to SQL, but instead of operating on database tables and columns, it operates on Java classes and objects.

JPQL queries are written against the entity objects and their fields rather than directly against database tables and columns. This allows developers to write database queries in an object-oriented fashion.

While JPQL is designed to be familiar to those who know [[Structured Query Language|SQL]], it uses the entity model of the application instead of the actual database tables. For example, a JPQL query might look like `SELECT c FROM Customer c` where `Customer` is a Java entity.

JPQL is part of the JPA specification and is used for querying the entities managed by JPA. It's a key component for retrieving entities based on various criteria. JPQL supports named parameters in queries, which enhances readability and maintainability. For example, `SELECT c FROM Customer c WHERE c.name = :name`.

JPQL supports aggregate functions like `COUNT`, `MIN`, `MAX`, `SUM`, and `AVG`, similar to SQL. Since JPQL works with entities, it is database-independent. The same JPQL query can run across different database systems without modification.

JPQL allows querying over relationships defined in the entity model. For example, you can easily join across various related entities (like fetching all orders for a customer). In a JPA application, JPQL queries are executed via the `EntityManager` interface, which provides methods like `createQuery` to create and execute JPQL queries.

While powerful, JPQL has limitations compared to native SQL, especially in terms of database-specific features and optimizations. For more complex queries, sometimes native SQL queries might be preferable.

JPA also provides the Criteria API as an alternative to JPQL for building queries programmatically. This is useful for constructing dynamic queries where the structure of the query depends on runtime conditions.