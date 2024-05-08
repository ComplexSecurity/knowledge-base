OS Command Injection is a type of security vulnerability that occurs when an attacker is able to execute arbitrary operating system commands on a server due to insufficient input validation in a web application. This vulnerability is exploited by injecting malicious commands into inputs that are expected to be part of system commands executed by the server.

The vulnerability arises in web applications that use user input to construct operating system commands without [Input Sanitization|proper validation or sanitization](). This can happen in applications that need to execute system-level commands based on user inputs.

An attacker manipulates the input fields (like form inputs, URL parameters, etc.) to include additional commands or alterations to the intended command. This manipulation can alter the execution flow or introduce new commands.

If the application does not properly sanitize user inputs, the web server executes the injected command with the same privileges as the application itself. This can lead to various malicious activities, such as accessing or modifying files, accessing private information, installing malware, or taking control of the server.

The extent of exploitation depends on the permissions of the user under which the web application runs. In severe cases, it can lead to a complete system takeover.
