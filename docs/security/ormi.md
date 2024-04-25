ORM Injection is a type of attack targeting applications that use [[Object-Relational Mapping]] (ORM) libraries to interact with databases. ORM is a technique that allows developers to manage database data as objects in programming languages like [[Java]], [[CSharp|C#]] and [[Python]], etc. 

ORM Injection exploits vulnerabilities where user inputs are improperly sanitized before being passed to ORM methods or functions.

Similar to [[SQL Injection]], ORM Injection occurs when an attacker manipulates inputs to inject malicious code or queries. However, instead of targeting raw SQL queries, ORM Injection targets the ORM query functions or methods.

ORMs often provide methods for building queries without the need to write raw SQL. If these methods are used with unsanitized inputs, attackers can manipulate them to alter query logic or execute unintended commands.

1. Impacts of ORM Injection:
    - **Unauthorized Data Access**: Attackers could gain access to sensitive data stored in the database.
    - **Data Modification or Deletion**: In cases where ORM allows data modification, an attack could lead to altering or deleting data.
    - **Bypassing Business Logic**: ORM Injection might bypass application business logic, leading to unauthorized actions.

In a Python app using an ORM like SQLAlchemy an example of vulnerable code may be:

```python
user_input = request.form['user_input']
query = session.query(User).filter("username = '{}'".format(user_input))
```

> [!info]
> If `user_input` is not properly sanitized, it could be exploited to manipulate the query.

