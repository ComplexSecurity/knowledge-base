Object-Relational Mapping (ORM) is a programming technique used for converting data between incompatible type systems in object-oriented programming languages. It's a common approach in software development that allows developers to manipulate database data as objects, making it easier to write database-agnostic code.

In ORM, classes in your application (often representing entities) are mapped to database tables, and instances of those classes (objects) are tied to rows in those tables. This mapping abstracts the underlying database structure.

ORM provides a high-level abstraction over relational database operations. Developers can interact with databases using their native programming language rather than [[Structured Query Language|SQL]], reducing the need for database-specific SQL queries.

Most modern programming languages like [[Java]], [[Python]], [[CSharp|C#]], [[PHP]], [[Ruby]], and others have popular ORM frameworks. ORM facilitates [[CRUD API|CRUD]] (Create, Read, Update, Delete) operations on the database by providing methods to easily handle these tasks without manually writing SQL queries.

Many ORM tools allow for a level of database independence, meaning the same code can be used with different database systems (like [[MySQL (KB)|MySQL]], [[PostgreSQL]], [[Microsoft SQL Server|SQL Server]], etc.) with minimal or no changes.

ORM can significantly reduce the amount of boilerplate code required to interact with a database, speeding up development and potentially reducing errors. While ORMs allow for working with data as objects, they also usually provide a way to write complex queries, often through a Query Language or Builder, which is then translated to SQL.

While ORMs add convenience, they can sometimes lead to less efficient database queries compared to finely-tuned SQL, especially in complex scenarios. This is sometimes referred to as the "Object-Relational Impedance Mismatch".
