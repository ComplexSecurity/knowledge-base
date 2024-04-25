NGINX (pronounced “engine X”) is open-source web server software designed to handle a high number of connections simultaneously. These characteristics make it one of the most powerful and scalable server software options on the market:

NGINX is often used as a [[reverse proxy]]. This means you’ll typically find it stationed behind a [[firewall]] in a private network, where it forwards client requests to the appropriate server.
 
NGINX also acts as a load balancer. This means it distributes requests across multiple servers so that they won’t become overloaded. In turn, this setup leads to faster web speeds for users.

Nginx is built to offer low memory usage and high concurrency. Rather than creating new processes for each web request, Nginx uses an asynchronous, event-driven approach where requests are handled in a single thread.

With Nginx, one master process can control multiple worker processes. The master maintains the worker processes, while the workers do the actual processing. Because Nginx is asynchronous, each request can be executed by the worker concurrently without blocking other requests.

Some common features seen in Nginx include:

- Reverse proxy with caching
- IPv6
- Load balancing
- FastCGI support with caching
- WebSockets
- Handling of static files, index files, and auto-indexing
- TLS/SSL with SNI