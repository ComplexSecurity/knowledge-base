A WebSocket is a communication protocol that provides full-duplex communication channels over a single [TCP](../networking/tcp.md) connection. It enables real-time, event-driven communication between a client and a server.

Unlike traditional [HTTP](../web/http.md), which follows a request-response model, WebSockets allow bi-directional communication. This means that the client and the server can send data to each other anytime without continuous polling.

WebSockets are a bi-directional, full duplex communications protocol initiated over HTTP. They are commonly used in modern web applications for streaming data and other asynchronous traffic.

Most communication between web browsers and web sites uses HTTP. With HTTP, the client sends a request and the server returns a response. Typically, the response occurs immediately, and the transaction is complete. Even if the network connection stays open, this will be used for a separate transaction of a request and a response.

Some modern web sites use WebSockets. WebSocket connections are initiated over HTTP and are typically long-lived. Messages can be sent in either direction at any time and are not transactional in nature. The connection will normally stay open and idle until either the client or the server is ready to send a message.

WebSockets are particularly useful in situations where low-latency or server-initiated messages are required, such as real-time feeds of financial data.
