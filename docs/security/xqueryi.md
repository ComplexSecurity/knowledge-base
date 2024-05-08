XQuery Injection is a security vulnerability that occurs in applications that use [XQuery]() ([Extensible Markup Language|XML]() Query Language) to interact with XML databases. Similar to [SQL Injection](), XQuery Injection involves the manipulation of XQuery expressions through unvalidated user input. Attackers exploit this vulnerability to execute malicious queries, access unauthorized data, or compromise the integrity of the database.

The vulnerability arises when an application constructs XQuery expressions by concatenating user-supplied input without proper validation or sanitization. Attackers can craft input to alter the intended query, leading to unintended database actions or data exposure.

Consider a web application that uses XQuery to fetch user information from an XML database:

```xquery
let $user := request:get-parameter("username")
let $query := "doc('users.xml')/users/user[name=$user]"
return eval($query)
```

If the `$user` parameter is taken directly from user input without validation, an attacker could inject a payload that alters the query, potentially accessing all user data.
