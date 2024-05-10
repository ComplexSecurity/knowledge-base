Tplmap is a penetration testing tool designed for automating the identification and exploitation of [Server-Side Template Injection (SSTI)](../security/ssti.md) vulnerabilities in web applications. SSTI vulnerabilities occur when user input is directly embedded into server-side templates without proper validation or sanitization, allowing attackers to inject and execute arbitrary code on the server.

Tplmap is designed to be template engine agnostic, meaning it can identify and exploit SSTI vulnerabilities in various template engines used by web applications. It supports popular template engines such as [Jinja2](../web/jinja2.md), [Mako](../web/mako.md), [Smarty](../web/smarty.md), and more.

The tool automates the process of detecting SSTI vulnerabilities by analyzing how user-supplied input is processed within the server-side templates. It aims to identify injection points where payloads can be injected for exploitation. 

Tplmap provides capabilities for exploiting identified SSTI vulnerabilities by injecting payloads and observing the resulting output. This allows penetration testers to assess the impact of the vulnerability and understand the extent of code execution.

Tplmap comes with a set of predefined payloads that can be used for testing and exploiting SSTI vulnerabilities. These payloads are crafted to trigger code execution and showcase the severity of the vulnerability. Tplmap offers an interactive mode that enables penetration testers to manually explore and exploit SSTI vulnerabilities. This mode allows for more fine-tuned testing and analysis.

Tplmap supports template engines used in different programming languages, making it versatile for testing web applications built with various technologies.

A usage example:

```bash
tplmap -u "http://example.com/page?input={{INJECTION_POINT}}" --os-cmd 'uname -a'
```

Tplmap is instructed to test the specified URL with the provided injection point (`{{INJECTION_POINT}}`) and execute the operating system command `uname -a` to check the underlying system details.