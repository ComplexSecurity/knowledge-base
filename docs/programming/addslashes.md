The addslashes function in [PHP](../programming/php.md) is a built-in function used to escape certain characters in a string by prefixing them with a backslash. This function is typically used to prepare a string for insertion into a database, particularly when dealing with strings that may contain quotes or other special characters that need to be escaped.

It escapes the following:

- Single quote (')
- Double quote (")
- Backslash (\\)
- NULL (the NULL byte)

An example usage may be:

```php
$unescaped_str = "O'Reilly & Associates";
$escaped_str = addslashes($unescaped_str);

// Output: O\'Reilly & Associates
echo $escaped_str;
```

In this example, the single quote in "O'Reilly" is prefixed with a backslash, making it safe for use in a SQL query, for instance.

While addslashes can escape certain characters, it should not be solely relied upon for preventing [SQL injection](../security/sqli.md) attacks. The use of prepared statements with parameterized queries is the recommended approach for database interaction in PHP to prevent SQL injection.

The addslashes function in PHP is not suitable for preventing [Cross-Site Scripting](../web/xss.md) (XSS) attacks. While addslashes is designed to escape certain characters (like single quotes, double quotes, backslashes, and NULL) by adding backslashes before them, it does not address the core requirements for mitigating XSS vulnerabilities.
