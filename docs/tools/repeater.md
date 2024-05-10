Burp Repeater is a tool within [Burp Suite](../tools/burpsuite.md), a comprehensive platform for web application security testing. Burp Repeater is designed for manual testing and analysis of individual HTTP and [WebSocket](../protocols/sockets.md) requests and responses. It allows security testers to modify and resend web requests in a controlled manner. 

The primary function of Burp Repeater is to allow security testers to manually edit and resend individual HTTP/S requests to a web server without the need for re-navigating through the application in a browser.

Burp Repeater is used to thoroughly test the security of web applications by examining how they respond to modified requests, which can include altered parameters, headers, method types, and more

It is particularly useful for exploiting vulnerabilities like [SQL injection](../security/sqli.md), [cross-site scripting](../web/xss.md), parameter tampering, and others.

After modifying and resending requests, Burp Repeater captures the server's response, allowing testers to analyze the impact of their changes. It provides detailed information on HTTP status codes, headers, and the response body.

Burp Repeater's interface is straightforward, making it easy to change request parameters and quickly observe the server's response. Requests captured by other Burp Suite tools, like [Burp Proxy](../tools/proxy.md) or [Burp Scanner](../tools/scanner.md), can be sent to Burp Repeater for further examination and manipulation.

Testers can use Burp Repeater to try out different inputs and attack vectors, making it an essential tool for identifying and exploiting vulnerabilities in a targeted and precise manner. Burp Repeater allows testers to open multiple instances (tabs) for comparing the outcomes of different request modifications side by side.

In addition to HTTP/S, Burp Repeater supports testing of WebSocket communication, enabling analysis of real-time, interactive communication sessions.

By enabling manual control over request editing and analysis, Burp Repeater speeds up the process of vulnerability verification and exploitation.