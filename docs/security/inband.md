In-band [SQL injection]() is a type of SQL injection where the attacker uses the same communication channel to both launch the attack and gather results. It's one of the most common types of SQL injection attacks. There are two main types of in-band SQL injection:

1. [Error-Based Injection|Error-based SQL Injection]() - This method involves the attacker intentionally making incorrect SQL queries to the database. The database then generates error messages which may contain useful information about the database's structure. These error messages are used by the attacker to further exploit the system.
2. [UNION-Based injection|Union-based SQL Injection]() - In this method, the attacker uses the [UNION queries|UNION]() SQL operator to combine a malicious query with a legitimate query. The results of the malicious query are returned as part of the [HTTP Protocol]() response, which the attacker can use to extract data from the database.

