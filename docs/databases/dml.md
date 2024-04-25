Data Manipulation Language (DML) is a subset of SQL ([[Structured Query Language]]) used for adding (inserting), deleting, and modifying (updating) data in a database. DML is one of the key elements of SQL and is essential for managing and manipulating the data stored in relational databases.

DML primarily includes three types of operations:

- **Insert**: Adding new rows of data to a table.
- **Update**: Modifying existing data within a table.
- **Delete**: Removing data from a table.

The `INSERT` statement is used to add new records to a database table. It allows specifying both the columns and the values to insert. The `UPDATE` statement modifies existing records in a table. It typically involves specifying a condition to identify which rows to update and what new values should be assigned to specific columns.

The `DELETE` statement removes existing records from a table, usually based on a condition that specifies which rows should be deleted. DML operations often involve transactional control commands like `COMMIT`, `ROLLBACK`, and `SAVEPOINT`. These commands manage transaction processing, ensuring data integrity and consistency.

DML statements are considered non-destructive in terms of database schema. They modify the data within the tables without altering the table structure itself. DML statements are fundamental to [[CRUD API|CRUD]] (Create, Read, Update, Delete) operations in database systems, forming the backbone of most database interactions in applications.

When performing DML operations, especially in application development, it’s important to guard against SQL injection attacks. This is often achieved through the use of prepared statements or ORM ([[Object-Relational Mapping]]) frameworks.

DML commands are used in various [[Database Management Systems]] (DBMS), like [[MySQL (KB)|MySQL]], [[Oracle Database|Oracle]], [[Microsoft SQL Server|SQL Server]], [[PostgreSQL]], and others, making them a core skill for database professionals and developers.
