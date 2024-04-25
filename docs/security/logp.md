Log poisoning is a technique used in cyber attacks, often in conjunction with other vulnerabilities like [[Local File Inclusion]] (LFI), to execute arbitrary code or commands on a web server. It primarily involves manipulating log files that the server writes and then exploiting these files through other vulnerabilities.

The attacker injects malicious code or script into a log file. This can be done in several ways, such as by entering malicious strings into input fields that are logged (like [[user-agent]], referrer, or error messages) or by making requests that get logged with the attacker's control over some part of the request (like the request URL or headers).

If the web application is vulnerable to LFI, the attacker can include the log file in the response. Since log files contain the attacker's injected code, this code gets executed when the included log file is processed by the server.

Some common scenarios include:

- **Web Server Logs**: Injecting scripts or [[PHP]] code into access or error logs of the web server. For instance, by accessing a URL with a PHP code snippet in it, knowing that the URL will be logged.
- **Application Logs**: Manipulating input fields that are known to be logged by the application, such as user login fields, search queries, etc.

As an example scenario:

The attacker visits a web page and sets their User-Agent header to a PHP code snippet, such as `<?php system($_GET['cmd']); ?>`. The web server logs this request, including the User-Agent string. If there's an LFI vulnerability, the attacker can request a page that includes the web server's access log. When the server processes the included log file, the PHP code from the User-Agent string is executed, allowing the attacker to run commands on the server.



