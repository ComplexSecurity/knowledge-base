In the context of web application penetration testing and [SQL injection](), "UNION queries" refer to a specific technique used to extract additional information from a database by combining the results of two or more SELECT statements into a single result. This technique is particularly important in the exploitation of SQL injection vulnerabilities.

The UNION SQL operator is used to combine the results of two or more SELECT statements into a single result set. This can be exploited in SQL injection attacks to extract data from different database tables or columns that weren't intended to be displayed.

For this to work, each SELECT statement within the UNION must have the same number of columns in the result sets with similar data types.

As an example, consider a web application that uses a query like **SELECT name, age FROM users WHERE id = \[input]** to retrieve user information. An attacker could input something like **1 UNION SELECT username, password FROM admin**.

If the application is vulnerable, this would cause it to return a dataset that combines the intended user information with usernames and passwords from the admin table.
