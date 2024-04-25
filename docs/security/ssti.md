Server-Side Template Injection (SSTI) is a type of web security vulnerability that occurs when an attacker is able to inject malicious code into a server-side template, leading to the execution of unintended commands or code on the server. This vulnerability exploits web applications that use templating engines to dynamically generate [[HTML]] pages.

Template engines are used in web development to separate HTML structure from business logic. They allow server-side variables and expressions to be embedded in HTML, which the server then processes to generate the final HTML page. Examples include [[Jinja2]] for [[Python]], [[ERB]] for [[Ruby]], and [[Smarty]] for [[PHP]].

SSTI vulnerabilities arise when user input is improperly [[Input Sanitization|sanitized]] before being included in a template. This allows attackers to inject malicious template code, which the server then executes. The impact depends on the template engine and the server’s configuration.

In severe cases, SSTI can lead to [[Knowledge Base/Remote Code Execution|arbitrary code execution]] on the server. SSTI can be used to access sensitive data stored on the server, such as database credentials. Malicious template injections could cause server crashes or significant performance degradation.

A web application uses user input to construct a response using a template engine. If the input is not properly sanitized, an attacker could inject template directives, leading to unintended code execution.

For instance, in a Python application using Jinja2, injecting `{{ 7*'7' }}` would cause the server to evaluate and execute it, rendering `7777777`.