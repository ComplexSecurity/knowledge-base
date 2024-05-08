Web Cache Poisoning is a security vulnerability in web applications and their caching mechanisms. It involves exploiting the behavior of a web cache to distribute malicious content to users.

During web application penetration testing, identifying and exploiting web cache poisoning can reveal how attackers might manipulate cached web content to their advantage.

Web caches store copies of web documents (like [HTML]() pages and images) to improve response times for users. They can be located at various points in the network, including browser caches, server-side caches, and CDN ([Content Delivery Network]()) caches.

The attacker sends a specially crafted [HTTP Protocol|HTTP]() request to the server. This request includes an anomaly (like a custom header or a manipulated parameter) that the caching mechanism does not properly handle.

If the server response to this request is cacheable, the cache stores the malicious response. Subsequent users requesting the same resource receive the poisoned (malicious) content from the cache.

Attackers exploit discrepancies between how an application server processes requests and how caches determine what is cacheable. For example, if a web server ignores an unrecognized query parameter but the cache considers it when caching content, this can be exploited to poison the cache.

Some impacts of it include:

- Content Manipulation: malicious scripts or links could be served to users, leading to [Cross-Site Scripting]() (XSS) attacks or redirecting users to phishing sites.
- Denial of Service: cache poisoning can be used to make a website unavailable or to serve incorrect content.
