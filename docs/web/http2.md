HTTP/2 is the second major version of the [[HTTP Protocol|HTTP]] network protocol, used by the World Wide Web. It was developed by the HTTP Working Group of the Internet Engineering Task Force (IETF) and was published in 2015.

HTTP/2, developed as an improvement over [[HTTP1.1|HTTP/1.1]], brings significant advancements aimed at efficiency and speed. Key enhancements include:

1. **Binary Framing Layer**: This change from HTTP/1.1's text-based format helps to more efficiently parse, multiplex, and prioritize streams.
2. **Multiplexing of Requests**: HTTP/2 can send multiple requests for data in parallel over a single TCP connection. This drastically reduces the latency that was caused by HTTP/1.1's one-request-per-connection model.
3. **Stream Prioritization**: Clients can prioritize streams, allowing more important resources to be sent earlier.
4. **Server Push**: Servers can proactively send resources to a client's cache for future use, improving load times.
5. **Header Compression**: HTTP/2 compresses headers using the [[HPACK]] compression format, reducing overhead.
6. **Enhanced Security**: Although not inherent in the protocol, HTTP/2 is often implemented alongside [[TLS]] (Transport Layer Security), encouraging encrypted connections.
