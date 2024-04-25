LDAP Injection is a type of cyber attack that exploits vulnerabilities in a web application's software when it constructs LDAP ([[Lightweight Directory Access Protocol]]) statements based on user input. LDAP is used for accessing and maintaining distributed directory information services over an Internet Protocol network. 

In an LDAP injection attack, the attacker manipulates a web application's input fields to inject and execute malicious LDAP statements. These statements can modify LDAP queries executed by the application, potentially allowing unauthorized access to sensitive information in the LDAP directory.

Similar to [[SQL Injection]], LDAP Injection occurs when user-supplied data is not properly sanitized before being added to an LDAP query. Attackers exploit this vulnerability to alter LDAP statements or add new criteria.

Attackers might gain unauthorized access to sensitive data stored in the LDAP directory, such as usernames, passwords, and other personally identifiable information. In more severe cases, attackers could modify or delete information within the LDAP directory, impacting the integrity of the system.

A web application might use user input to construct an LDAP query for authentication. If this input is not properly sanitized, an attacker could modify the LDAP filter. For instance, entering a wildcard character (\*) might return all user entries, bypassing authentication controls.

