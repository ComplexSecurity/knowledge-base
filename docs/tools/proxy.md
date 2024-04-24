Burp Proxy, part of the [[Burp Suite]], is a tool used for intercepting and manipulating HTTP requests and responses. It acts as an intermediary between the user's browser and web servers, allowing security testers to inspect and modify the traffic to identify and exploit security vulnerabilities in web applications.

Burp Proxy intercepts [[HTTP Protocol|HTTP]] and [[HTTPS Protocol|HTTPS]] requests and responses between the client browser and the web server. This allows users to view and modify the requests sent by the browser and the responses sent by the server.

It is widely used for security testing and analysis of web applications. This includes tasks such as tampering with requests, replaying requests, modifying headers, post parameters, and observing the application's responses.

To use Burp Proxy, the user's browser must be configured to route traffic through it. This typically involves setting the browser's proxy settings to the host and port where Burp Proxy is listening (by default, it's localhost and port 8080).

For HTTPS traffic, Burp Proxy uses its own self-signed [[Certificate Authorities (CAs)|CA]] certificate. The user must install this certificate in their browser to avoid security warnings and to intercept HTTPS traffic properly.

Traffic intercepted by Burp Proxy can be sent to other tools within the Burp Suite for further analysis or exploitation, such as [[Burp Scanner]], [[Burp Intruder]], and [[Burp Repeater]]. Burp Proxy provides a user-friendly interface for viewing and modifying HTTP/S traffic. It displays requests and responses in a readable format, with syntax highlighting for [[HTML]], [[JavaScript]], [[CSS]], and [[Extensible Markup Language|XML]].

Common use cases include modifying sessions, testing for vulnerabilities like [[Cross-Site Scripting]] (XSS) or [[SQL Injection]], and understanding the application's logic and data flow. It allows real-time analysis of the traffic, enabling testers to observe how the application responds to various manipulations instantly.

While automated tools like Burp Scanner are used for vulnerability scanning, Burp Proxy is essential for manual testing, where the tester's expertise can identify issues that automated tools might miss.

