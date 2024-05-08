Remote File Inclusion (RFI) is a type of vulnerability commonly found in web applications. It allows an attacker to include a remote file, usually through a script on the web server, into the web application. 

This vulnerability occurs when a web application dynamically includes external files or scripts from a [Uniform Resource Locator|URL]() that is not properly sanitized.

RFI vulnerabilities typically arise in web applications that use script-based languages like [PHP](), [JSP](), or [ASP.NET|ASP](). These applications often include files or scripts to extend their functionalities. The vulnerability is exploited when the application takes user input (like a URL or file path) without proper validation or sanitization and uses this input to include a script or file.

An attacker can exploit this by supplying a URL or path to a malicious file. If the application includes this file in its execution, it can lead to severe consequences.