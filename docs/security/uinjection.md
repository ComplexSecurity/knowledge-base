Union-based [[SQL injection]] is a type of in-band SQL injection attack that leverages the [[UNION queries|UNION]] SQL operator. This operator is used to combine the results of two or more SELECT statements into a single result set.

In the context of a SQL injection attack, the attacker uses the UNION operator to append a malicious SQL query to a legitimate query made by the application.

The attacker first identifies input fields in the application that are vulnerable to SQL injection. The attacker then crafts a SQL query that they wish to execute on the database. This query is designed to extract data from the database that the attacker wants to access.

The attacker combines their malicious query with the legitimate query using the UNION operator. For the UNION to work, the original query and the injected query must return the same number of columns and compatible data types. This is often achieved through trial and error.

The combined query is executed by the database. If successful, the database returns a dataset that includes results from both the legitimate and the injected queries. This result is then sent back to the user within the application's response.

Consider a site where the URL is used to query the database for user details:

```bash
http://example.com/userdetails?id=1
```

The SQL query might be:

```sql
SELECT name, email FROM users WHERE id = 1;
```

An attacker can modify the URL to:

```bash
http://example.com/userdetails?id=1 UNION SELECT username, password FROM admin_users;
```

Which would result in a SQL query like:

```sql
SELECT name, email FROM users WHERE id = 1 UNION SELECT username, password FROM admin_users;
```

If the query is executed, it would return data from both the '**users**' and '**admin_users**' tables.
