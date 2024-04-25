Data Query Language (DQL) is a subset of SQL ([[Structured Query Language]]) used specifically for querying and retrieving data from databases. Unlike [[Data Manipulation Language (DML)]], which includes commands for inserting, updating, and deleting data, DQL is focused solely on the retrieval of data.

The primary command in DQL is the `SELECT` statement. It is used to fetch data from a database table, which then returns this data in the form of a result set. DQL allows for specifying particular columns to retrieve, filtering data using conditions (`WHERE` clause), sorting the result set (`ORDER BY`), grouping data for aggregate functions (`GROUP BY`), and having clauses to filter groups (`HAVING` clause).

Through DQL, you can perform various types of joins (like INNER JOIN, LEFT JOIN, RIGHT JOIN, FULL JOIN) to combine rows from two or more tables based on related columns between them. DQL supports the use of subqueries, where a query is nested inside another query, allowing for complex data retrieval operations.

DQL operations are read-only, meaning they don’t modify the data in the database. They are used solely to query and extract data. DQL is extensively used in generating reports, performing data analysis, and creating dashboards where data retrieval is required without the need to change the underlying data.

DQL can be used with various SQL functions, including string functions, numeric functions, date functions, and more, to manipulate the output format of the retrieved data. Knowledge of DQL is fundamental for database professionals, analysts, and anyone working with SQL databases, as it forms the basis of data extraction for analysis and decision-making.
