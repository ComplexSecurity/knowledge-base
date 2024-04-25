Head-of-Line (HOL) blocking is a performance issue that occurs in networking and computer systems. In the context of HTTP/1.x, it refers to the problem where a line of requests must wait for the first request to be completed and responded to before the next can be processed. 

This happens because HTTP/1.x handles requests sequentially on each [[Transmission Control Protocol|TCP]] connection. With HOL blocking, even if subsequent requests are ready to be processed, they are blocked by the first request, leading to inefficiencies and increased latency. This issue is significantly mitigated in [[HTTP2|HTTP/2]] through the use of multiplexing, where multiple requests can be sent and responses received asynchronously over a single connection.

