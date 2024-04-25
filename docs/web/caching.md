Caching of web content refers to the practice of storing copies of web resources (such as [[HTML]] pages, images, stylesheets, and scripts) at various points in the network, allowing subsequent requests for the same content to be served more quickly. Caching is an essential mechanism for optimizing web performance, reducing latency, and minimizing the load on web servers.

A cache is a temporary storage location that holds copies of frequently accessed data to speed up retrieval. Web browsers maintain a local cache on users' devices to store copies of recently visited web pages and associated resources. When a user revisits a page, the browser can retrieve resources from the local cache instead of fetching them from the web server.

[[HTTP Protocol|HTTP]], the protocol used for transferring data on the web, supports caching mechanisms defined by headers in the HTTP response.

Common HTTP headers related to caching include:

- **Cache-Control:** Specifies directives for caching mechanisms in both requests and responses.
- **Expires:** Indicates a specific date and time after which the response is considered stale.
- **Last-Modified:** Specifies the last modification date of the resource.
- **ETag:** A unique identifier for a specific version of a resource.

Cache-Control Directives:

- **public:** Indicates that the response may be cached by any cache (including proxies).
- **private:** Indicates that the response is intended for a single user and should not be stored by shared caches.
- **max-age:** Specifies the maximum amount of time (in seconds) a response can be considered fresh.
- **no-cache:** Requires caches to revalidate the content with the server before serving it.

[[Content Delivery Network]] (CDNs) cache static assets at strategically located servers worldwide. CDNs help distribute content closer to end-users, reducing latency and improving load times. Web servers can implement caching mechanisms to store generated content and reduce the need for dynamic processing.

!!! info
Popular web servers like [[Apache]] and [[Nginx]] support caching configurations.

Entire HTML pages can be cached to avoid reprocessing on the server for each request. This is particularly useful for static or relatively static content. When content is updated, cache invalidation mechanisms ensure that stale cached copies are purged. Techniques include changing cache keys, versioning resources, or using cache purging tools.
