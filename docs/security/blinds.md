Blind SQL injection is a type of [SQL injection]() attack where the attacker cannot see the result of a query directly. This lack of direct feedback makes the attack more challenging. 

However, attackers can still infer information about the database by observing the behavior of the application or the time it takes for the query to execute. Blind SQL injections are classified into two main types:

1. [Blind Boolean Injection|Boolean-Based Blind SQL Injection]() - In this method, the attacker sends a SQL query to the database which forces the application to return a different result depending on whether the query is true or false. By observing changes in the application's response or behavior (like changes in the content, error messages, or even just a simple 'yes' or 'no' response), the attacker can infer whether the injected statement was true.
2. [Time-Based Boolean Injection|Time-Based Blind SQL Injection]() - In this technique, the attacker crafts a SQL query that causes the database to wait for a specified amount of time before responding. By measuring the time the application takes to respond, the attacker can determine whether a certain part of the SQL query was true or false.


