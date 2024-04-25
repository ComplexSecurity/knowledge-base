Inline queries, also known as inline SQL or dynamic SQL, refer to SQL commands that are constructed as strings within an application's code and then executed by a database.

These queries are dynamically built using input from users or other sources. In the context of [[SQL injection]], inline queries are particularly relevant because they can create vulnerabilities if not handled correctly.

Inline queries are often vulnerable to SQL injection attacks when user input is concatenated directly into the query string. Attackers can manipulate the input to alter the query's structure, executing unintended commands or accessing unauthorized data.

An example of a vulnerable inline query:

```sql
String query = "SELECT * FROM users WHERE username = '" + userInput + "'";
```

In this example, if `userInput` is not properly sanitized and contains something like `' OR '1'='1`, it could lead to a SQL injection.

Attackers exploit inline queries by injecting malicious SQL code into the query string. This can lead to various malicious actions, such as bypassing authentication, retrieving, modifying, or deleting data, and, in severe cases, compromising the entire database or associated system.

Inline queries often lack parameterization, a technique that separates SQL code from data inputs. Without parameterization, the query and data inputs are concatenated into a single string, making it easier for malicious inputs to alter the query structure.

