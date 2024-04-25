Undertow is a high-performance, lightweight web server written in [[Java]]. It is designed to be embeddable within applications and frameworks, making it a popular choice for building microservices and standalone web applications.

Undertow is designed to be easily embedded within Java applications. This makes it well-suited for microservices architectures, where lightweight and modular components are essential. Undertow is built with a focus on asynchronous and non-blocking I/O operations. This allows it to handle a large number of concurrent connections efficiently, making it suitable for high-performance scenarios.

Undertow provides native support for [[WebSockets|WebSocket]] communication. This enables real-time, bidirectional communication between clients and servers, making it suitable for applications with interactive features.

Undertow supports the HTTP/2 protocol, which is the latest version of the [[HTTP protocol]]. HTTP/2 introduces improvements in performance, multiplexing, and header compression over its predecessor, HTTP/1.1.

Undertow supports the Servlet 4.0 specification, which includes features such as HTTP/2 support, server push, and more. Servlets are a standard Java technology for building web applications. Undertow is designed with a modular architecture, allowing developers to choose and include only the components they need. This results in a smaller footprint and improved performance.

In addition to server-side WebSocket support, Undertow provides a WebSocket client API, allowing applications to initiate WebSocket connections to external services. Undertow is closely integrated with the JBoss ecosystem, and it is the default web server used by the WildFly application server. This integration provides seamless interoperability with other JBoss technologies.

Undertow includes security features such as [[SSL-TLS|SSL/TLS]] support for secure communication, integration with security realms, and support for authentication and authorization mechanisms. Undertow can be deployed in various scenarios, including as a standalone web server, embedded within applications, or as part of a larger application server environment.
