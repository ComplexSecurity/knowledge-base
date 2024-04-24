Blind boolean [[SQL injection]] are a subtype of [[Blind Injections|blind SQL injection]] attacks. In these attacks, the attacker cannot see direct data outputs from the database, such as in error-based or union-based SQL injections. Instead, they infer information about the database by sending a series of true or false queries and observing how the application's responses differ based on these conditions. 

The attacker crafts a SQL query that incorporates a condition which evaluates to either true or false. They rely on observing how the application behaves when the condition is met (true) versus when it is not met (false).

As with other SQL injections, the attacker first identifies input fields (like search boxes, login forms, or URL parameters) that are directly used in SQL queries and are vulnerable to injection.

The attacker injects a SQL condition that is designed to be either true or false. For instance, they might inject a statement like `1=1` (which is always true) or `1=2` (which is always false).

The key to blind boolean SQL injection is in observing how the application responds to these true or false conditions. If the application's response differs when a true condition is injected versus a false one, the attacker can infer that their injection is impacting the SQL query.

By iteratively refining these true or false conditions and observing the application's behavior, an attacker can extract data from the database, character by character.

For example, consider a login form:

```sql
SELECT * FROM users WHERE username = '[user_input]';
```

The attacker might input **admin' AND substring(password,1,1)='a**. If the application behaves differently when the first character of the admin's password is 'a', the attacker learns that information. They repeat this process for each character of the password.