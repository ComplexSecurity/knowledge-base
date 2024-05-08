AJP, short for Apache JServ Protocol, is a binary protocol that was designed to allow a standalone web server to communicate with an application server that executes [Java Servlets](../misc/servlets.md) and [JavaServer Pages (JSP)](../misc/jsp.md). Initially developed as part of the Apache JServ project, AJP has evolved and is commonly used with Apache Tomcat and other application servers.

The primary purpose of AJP is to allow efficient communication between a web server (like [Apache](../web/apache.md) HTTP Server) and an application server (like [Apache Tomcat](../misc/tomcat.md)). This is typically used in environments where you have web server fronting an application server.

AJP is a binary protocol, making it more efficient than [HTTP](../web/http.md) for server-to-server communication, especially for forwarding requests and responses. In many configurations, Apache HTTP Server serves static content directly and forwards requests for dynamic content (like Servlets and JSPs) to an Apache Tomcat (or other application server) instance via AJP.

AJP is often used in load-balanced environments where multiple application server instances are behind a web server or a [Load Balancer](../web/loadb.md). AJP has several versions, with AJP13 (or AJP v1.3) being the most commonly used. It operates over [TCP](../networking/tcp.md) and uses a default port of 8009.

Setting up AJP typically involves configuring both the web server and the application server to enable them to communicate over the AJP protocol. 

AJP connections should be secured, especially in network environments where the traffic might pass through untrusted networks. Recent security concerns have led to increased scrutiny of AJP configurations to prevent unauthorized access.

With the rise of more integrated application servers that can efficiently serve both static and dynamic content, the use of AJP has become less common. However, it is still used in certain legacy systems or in specific architectural scenarios.