SQL ([[Structured Query Language]]) statements are the means by which users interact with a relational database to perform various operations. 

SQL is a domain-specific language used in programming and designed for managing and manipulating data held in a [[relational database management system]] (RDBMS). SQL statements are used to execute tasks such as updating data on a database or retrieving data from a database. There are several types of SQL statements, broadly categorized into the following groups:

1. **Data Definition Language (DDL)**: These statements define the database structure or schema. Some common DDL statements include:
    - `CREATE`: Used to create a new table or database.
    - `ALTER`: Used to modify an existing database object, like adding a column to a table.
    - `DROP`: Used to delete an entire table or database.
    - `TRUNCATE`: Used to remove all records from a table, including all spaces allocated for the records.
2. **Data Manipulation Language (DML)**: These statements are used for managing data within schema objects. Some common DML statements include:
    - `SELECT`: Used to retrieve data from a database.
    - `INSERT`: Used to insert data into a table.
    - `UPDATE`: Used to update existing data within a table.
    - `DELETE`: Used to delete records from a database table.
3. **Data Control Language (DCL)**: These statements are used to control access to data in the database. Common DCL statements include:
    - `GRANT`: Used to give user access privileges to a database.
    - `REVOKE`: Used to withdraw access privileges given with the GRANT command.
4. **Transaction Control Language (TCL)**: These statements are used to manage the changes made by DML statements. They allow transactions to be grouped together. Common TCL statements include:
    - `COMMIT`: Used to save the work done.
    - `ROLLBACK`: Used to undo the work that has not been saved.
    - `SAVEPOINT`: Used to identify a point in a transaction to which you can later roll back.