Function Injection is a type of security vulnerability in web applications, particularly relevant in languages like [[PHP]], where code execution is highly dynamic. It occurs when an application allows user input to influence the names of functions that are executed. This vulnerability can lead to serious consequences, including unauthorized [[Knowledge Base/Remote Code Execution|code execution]] and compromise of the server.

In languages like PHP, functions can be called dynamically using variable function names. For instance, if you have a variable `$func` containing the string 'execute', calling `$func()` would be equivalent to calling `execute()`.

Function injection exploits occur when the application improperly allows user input to determine which function is called. If an attacker can control the name of the function being called, they could execute any function within the application's scope, including built-in PHP functions.

An example of vulnerable code:

```php
$function_name = $_GET['func'];
$function_name(); // Dangerous: Calls a function based on user input
```

Some potential risks include:

- **Arbitrary Code Execution**: An attacker could execute functions that modify or leak data, manipulate files, or perform other malicious actions.
- **Escalating Privileges**: If combined with other vulnerabilities, function injection could lead to [[privilege escalation]], allowing an attacker to perform actions as a more privileged user.

