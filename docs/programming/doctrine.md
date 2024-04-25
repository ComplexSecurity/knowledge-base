Doctrine is an [Object-Relational Mapping (ORM)](../programming/orp.md) system for [PHP](../programming/php.md). It is a set of PHP libraries and tools that provide an abstraction layer for database interactions, allowing developers to work with databases using object-oriented principles rather than [SQL](../programming/sql.md) queries. Doctrine aims to simplify database access and manipulation, improve code maintainability, and enhance the overall development process.

Doctrine allows developers to define the mapping between PHP objects (entities) and database tables. This is done through annotations, [YAML](../misc/yaml.md), or [Extensible Markup Language](../programming/xml.md) configuration files. The mapping describes how the properties of an entity correspond to columns in a database table.

ORM is the core concept of Doctrine. It enables developers to interact with the database using PHP objects, eliminating the need to write raw SQL queries. Entities represent database records, and changes to these objects are automatically synchronized with the underlying database.

Doctrine provides a database abstraction layer that supports multiple [database management systems (DBMS)](../databases/dms.md), such as [MySQL](../databases/mysql.md), [PostgreSQL](../databases/postgres.md), [SQLite](../databases/sqlite.md), and others. This allows developers to switch between different database backends with minimal code changes.

[Doctrine Query Language (DQL)](../programming/dql.md) is a powerful SQL-like language specifically designed for querying object-oriented data. DQL allows developers to express queries in terms of their PHP entities and avoids the need for direct SQL queries in many cases.

Doctrine can generate database schemas based on the entity mappings, and it provides tools for database schema migration. This helps manage database changes over time, making it easier to evolve the database schema without losing data.

Doctrine supports various caching mechanisms to improve performance. It can cache metadata, query results, and other elements to reduce the need for repeated database queries. Doctrine includes an events system that allows developers to hook into specific points in the object lifecycle, enabling them to execute custom logic during certain operations (e.g., before or after an entity is persisted or removed).
