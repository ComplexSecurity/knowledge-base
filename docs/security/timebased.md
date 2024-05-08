Time-based [SQL injection]() is a subtype of [Blind Injections|blind SQL injection](). In these attacks, the attacker cannot directly see the data retrieved by their injected SQL query due to the lack of error messages or direct output. Instead, they gather information about the database by observing the response time of the application. 

The attacker crafts a SQL query that includes a command to pause or delay the database's response for a certain amount of time. Commonly used functions for this purpose are **SLEEP()** in [MySQL (KB)|MySQL](), **pg_sleep()** in [PostgreSQL](), or **WAITFOR DELAY** in [Microsoft SQL Server|SQL Server]().

The attacker injects a condition that, if true, triggers the delay. By measuring the time it takes for the application to respond, the attacker can infer whether the condition in their SQL query was true or false. If the response is delayed, the condition is true; if the response time is normal, the condition is false.

To extract data, the attacker systematically tests different conditions. For example, to guess a password, the attacker might inject conditions to check each character of the password one by one. This process is slow as it involves sending many requests and waiting for the response time for each.

Consider an app where the following SQL query is executed:

```sql
SELECT * FROM users WHERE username = '[user_input]';
```

An attacker might inject a statement like:

```sql
' OR IF((SELECT SUBSTRING(password, 1, 1) FROM users WHERE username = 'admin') = 'a', SLEEP(10), NULL) -- '
```

If the first character of the admin's password is 'a', the database will pause for 10 seconds, indicating to the attacker that they guessed correctly.

