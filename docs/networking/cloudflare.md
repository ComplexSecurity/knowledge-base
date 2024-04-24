Cloudflare acts as an intermediary between a [client]() and a [server](), using a reverse [proxy]() to mirror and cache websites. By storing web content for delivery on the closest edge server, it is able to optimize loading times. That also allows it to modify content, such as images and rich text, for better performance.

This intermediary design is also how Cloudflare offers a level of filtration for security. By sitting between the client and the hosting server, it can detect malicious traffic, intercept distributed denial-of-service attacks, deflect attacks from bots, remove bot traffic and limit spam.

Cloudflare is a [Content Delivery Network](). CDNs are an increasingly popular model across the internet because they solve an important problem: latency. They, at least in Cloudflare’s case, provide what’s known as an edge network. In short, an edge network creates a much closer entry point for data, rather than bouncing it between servers across the globe.

With 155 data centres around the world, Cloudflare works by caching a version of a customer’s website and any static resources, then delivering it to visitors based on their location.

That ensures the least amount of distance between a visitor and a website, which reduces latency, bandwidth and page load times. By moving the content and computational work closer, Cloudflare-powered websites can work faster.

The company’s [DNS](dns.md) services use the same network of data centers. Cloudflare offers authoritative DNS and public DNS resolver services. Both are offered as privacy and speed-first alternatives to internet service provider DNS servers. 

In addition to content delivery and DNS services, Cloudflare provides security as a service with DDoS protection, email obfuscation, web application firewall access and threat blocking. By sitting between a client and host, it can also filter traffic, reducing bot traffic and spam.
