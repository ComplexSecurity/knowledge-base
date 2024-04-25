Parameterized queries, also known as prepared statements, are a way of executing SQL queries in a more secure and efficient manner. They are used to execute the same SQL statement repeatedly with different parameters, and are especially important in preventing [[SQL injection]] attacks. 

The query is prepared by specifying the [[Structured Query Language|SQL]] command with placeholders for the parameters. These placeholders are typically represented by question marks (?) or named placeholders. For example: **SELECT * FROM users WHERE username = ?**.

Before execution, the parameters are bound to these placeholders. The values for these parameters are provided by the user or the application. The database then executes the query, substituting the placeholders with the provided parameter values in a safe way. 

The crucial point here is that the parameters are treated as data, not as part of the SQL command, which prevents them from being interpreted as SQL code.

An example in PHP may be:

```php
$stmt = $mysqli->prepare("SELECT * FROM users WHERE username = ?");
$stmt->bind_param("s", $username);
$username = 'exampleUser';
$stmt->execute();
$result = $stmt->get_result();
```

