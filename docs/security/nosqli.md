NoSQL injection is a type of security vulnerability that targets NoSQL databases. NoSQL databases, such as [[MongoDB]], [[CouchDB]], and [[Apache Cassandra|Cassandra]], are increasingly popular due to their scalability and flexibility in handling large volumes of unstructured data. 

However, just like SQL databases, they are susceptible to injection attacks, albeit in a different form.

Unlike [[SQL injection]], which exploits vulnerabilities in the SQL query syntax, NoSQL injection attacks target the NoSQL query language or the database's API. Since NoSQL databases do not use SQL, the attack vectors differ.

NoSQL injections typically occur when user inputs are not properly sanitized or validated before being passed to a database query. Attackers can manipulate these inputs to alter database queries, leading to unauthorized access or data manipulation.