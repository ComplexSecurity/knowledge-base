Environment Variable Injection is a security vulnerability that occurs when an application inadvertently allows external input to influence or overwrite environment variables. Since environment variables can control the behavior of software and the system, manipulating them can lead to various security issues.

This vulnerability arises when an attacker is able to inject or modify environment variables used by a program. It typically happens when user-supplied input is improperly sanitized, allowing the input to alter or define the values of environment variables.

Malicious environment variable values can lead to execution of arbitrary code if the application uses these variables to execute system commands. Attackers might change environment variables in a way that escalates their privileges on the system.

In a web application, consider a server-side script that sets an environment variable based on query parameters:

```php
putenv("LANG=" . $_GET['lang']);
```

If `$_GET['lang']` is not properly [[Input Sanitization|sanitized]], it can be exploited to inject malicious values.
