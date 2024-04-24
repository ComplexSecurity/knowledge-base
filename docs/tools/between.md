The "between" tamper script in [[SQLmap]] is a part of SQLmap's suite of tamper scripts, which are used to modify SQL queries in order to bypass [[Web Application Firewall (WAF)|web application firewalls (WAFs)]] or other security measures that might block malicious [[SQL injection]].

The "between" tamper script modifies the numeric payloads by changing the comparison operator in the SQL query. Instead of a direct comparison (like `id = 1`), it uses the `BETWEEN` operator to make the condition true. 

For example, `id = 1` might be changed to `id BETWEEN 1 AND 1`. This alteration can sometimes bypass filters or security rules that are looking for specific patterns in SQL queries.

SQLmap is primarily used for automating the process of detecting and exploiting SQL injection flaws in web applications. SQL injection is a type of attack that allows an attacker to interfere with the queries that an application makes to its database.

Some web application firewalls are configured to detect and block common SQL injection patterns. Tamper scripts like "between" are designed to alter these patterns in a way that might not be recognized by the security filters, allowing the SQL injection to proceed undetected.

Tamper scripts in SQLmap are used as command-line options. You can specify one or more tamper script names to be used during the attack process. These scripts are modular and can be combined to form more complex tampering strategies.