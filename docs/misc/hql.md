HQL, or Hibernate Query Language, is an object-oriented query language used by [[Hibernate]], a popular [[Object-Relational Mapping]] (ORM) framework in [[Java]]. HQL is similar to SQL ([[Structured Query Language]]) but operates on the domain model (objects) rather than directly on the database tables.

HQL queries are written against the Hibernate entity objects and their properties, not against the database tables and columns. This aligns with object-oriented programming principles. Since HQL operates at the object level, it abstracts the underlying database specifics. Hibernate translates HQL queries into the appropriate SQL queries for the underlying database, providing database independence.

The syntax of HQL is quite similar to SQL, making it familiar and easy to learn for developers who are already acquainted with SQL. HQL seamlessly handles relationships (like one-to-many, many-to-many) defined in the Hibernate domain model, allowing for easy querying across related entities.

HQL supports a wide range of SQL-like operations, including joins, where clauses, group by, having, etc., along with Hibernate-specific features like fetching strategies and pagination. HQL supports parameter binding, which helps in preventing SQL injection attacks and makes the queries more dynamic.

HQL works well with other features of Hibernate, such as caching, lazy loading, and transaction management. It can be used not only to retrieve complete entity objects but also to select individual attributes or a subset of an entity's attributes. Besides querying, HQL also supports [[Direct Manipulation Language (DML)]] style operations such as insert, update, and delete.

HQL is commonly used in Java applications that utilize Hibernate for ORM, simplifying the task of writing complex queries involving objects and their relationships.