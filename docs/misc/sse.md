Server-sent Events (SSE) is a technology where a browser receives automatic updates from a server via [[HTTP Protocol|HTTP]] connection. SSE is used to push real-time updates from the server to the client over a single, long-held HTTP connection. It's a part of HTML5 and is a simple way to send unidirectional data from the server to the client.

Unlike [[WebSockets]] which provide full-duplex communication, SSE is designed for unidirectional communication from the server to the client. This makes SSE simpler and more efficient for scenarios where only server-to-client communication is required.

SSE is used for applications that require real-time data from the server, such as live news feeds, sports scores, social media updates, or any other form of real-time data streaming. Once established, the SSE connection remains open, allowing the server to send data to the client at any time without the client having to make a new request each time.

SSE operates over standard HTTP and does not require a special protocol or server implementation. This makes it compatible with existing web infrastructure. SSE typically handles text-based data (like UTF-8) and sends messages in a simple, line-based format.

In [[JavaScript]], the EventSource interface is used to handle SSE connections. This allows web pages to listen to server-sent events and react accordingly. If an SSE connection is dropped, the browser automatically tries to reconnect to the server, which is a useful feature for maintaining a persistent connection even in unstable network conditions.

For use cases that only require server-to-client communication, SSE can be more efficient than WebSockets, as it's simpler and doesn't require a full protocol upgrade from HTTP. Implementing SSE on the server side involves setting the `Content-Type` of the response to `text/event-stream` and formatting the data according to the SSE specification.

SSE is supported by most modern browsers, but it’s important to check compatibility, especially with older browsers or certain mobile browsers.