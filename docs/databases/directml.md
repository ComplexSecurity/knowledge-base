Direct Manipulation Language (DML) is a term generally used in the context of databases, referring to a subset of SQL ([[Structured Query Language]]) used for adding, updating, and deleting data in a database. DML is concerned with the manipulation and handling of data records.

The `INSERT` statement in SQL is used to add new records to a table. It allows you to specify the table to insert into and the values for the fields of the new record. The `UPDATE` statement is used to modify existing records in a table. It can update one or multiple records based on a specified condition (WHERE clause).

The `DELETE` statement is used to remove records from a table. Like `UPDATE`, it can delete a single record or multiple records based on a condition. Although the `SELECT` statement is primarily used for querying and retrieving data from a database (and thus often associated with [[Data Query Language]], or DQL), it is sometimes included in DML discussions since it's about handling data.

DML operations often involve transaction control statements like `COMMIT`, `ROLLBACK`, and `SAVEPOINT`, which help in maintaining data integrity. DML statements are non-destructive, meaning they modify the data without altering the schema or structure of the database.

DML is used in various database operations across multiple domains, making it a fundamental aspect of database and application development. DML is a part of the functionality provided by [[Database Management Systems|DBMS]] like [[MySQL]], [[Oracle Database|Oracle]], [[Microsoft SQL Server|SQL Server]], [[PostgreSQL]], and others.

In the context of application development, DML is crucial for [[CRUD API|CRUD]] (Create, Read, Update, Delete) operations, which form the backbone of data handling in most applications. When executing DML statements, especially in application code, it’s important to guard against [[SQL injection]] attacks, typically by using prepared statements or ORM frameworks.
