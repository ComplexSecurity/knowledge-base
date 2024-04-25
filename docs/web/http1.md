HTTP/1.0 is the first version of the Hypertext Transfer Protocol ([[HTTP Protocol|HTTP]]) that was widely used for the World Wide Web. As a basic protocol, it established the foundation for web communication, allowing for the transfer of [[HTML]] documents and other resources over the internet.

HTTP/1.0 opens a new [[Transmission Control Protocol|TCP]] connection for each HTTP request/response cycle, leading to increased latency due to the overhead of establishing connections. Like all HTTP versions, it is stateless, meaning each request is independent and the server retains no information between requests.

HTTP/1.0 has more limited capabilities in headers compared to later versions, impacting functionalities like caching and authentication.

In contrast to other versions:

- [[HTTP1.1|HTTP/1.1]]: Introduced features like persistent connections (keeping connections open for multiple requests), chunked transfer encoding, and additional cache control options. It's more efficient in handling web traffic.
- [[HTTP2|HTTP/2]]: Further improves efficiency with features like multiplexing (multiple requests over a single connection), server push, and header compression. It's binary, rather than textual, making it more compact and faster to parse.