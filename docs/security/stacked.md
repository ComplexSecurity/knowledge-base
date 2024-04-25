Stacked queries, in the context of web application penetration testing and [[SQL injection]], refer to a technique used to execute multiple SQL commands in a single query. This approach is particularly relevant when exploiting SQL injection vulnerabilities.

In the context of SQL injection, stacked queries are a method where an attacker injects multiple SQL commands into a single SQL statement. This is often done by separating the commands with semicolons (;).

As an example, suppose a web application's form inputs are not properly sanitized. An attacker might input something like **1; DROP TABLE users;** into a form field. If vulnerable, the application will execute this as two SQL commands: 

The first command (1) might be harmless, but the second command (DROP TABLE users) could lead to destructive actions like deleting a database table.