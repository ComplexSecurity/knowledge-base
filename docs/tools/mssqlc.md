Impacket's `mssqlclient` is a script that provides a command-line interface to interact with [[Microsoft SQL Server]] (MSSQL). It's part of the [[Impacket]] suite, a collection of [[Python]] classes and scripts for working with network protocols. `mssqlclient` is particularly useful for database querying and operations in the context of network security assessment, penetration testing, and IT administration.

It allows for direct interaction with Microsoft SQL Server, enabling the execution of SQL queries and commands. It supports both Windows ([[NTLM]]) and SQL Server authentication methods, allowing it to be used in a variety of network environments. Some versions of `mssqlclient` support the execution of operating system commands through SQL Server, depending on the server configuration and permissions. It can be used to perform database operations such as data querying, schema exploration, and database administration tasks.

An example of how to use it:

```bash
python mssqlclient.py <USERNAME>:<PASSWORD>@<TARGET_IP> -windows-auth
```

- `<TARGET_IP>` is the IP address of the target MSSQL server.
- The `-windows-auth` flag is used for Windows (NTLM) authentication; omit this flag for standard SQL Server authentication.

>[!info]
>Once connected, you will be presented with an [[Structured Query Language|SQL]] command prompt where you can execute SQL queries and commands.

For example, to list the databases, you might use:

```sql
SQL> SELECT name FROM sys.databases;
```





