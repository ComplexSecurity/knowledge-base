A virtual host refers to a method used by web [[server|servers]], such as [[Apache]] HTTP Server or [[Nginx]], to host multiple websites or web applications on a single physical server.

Each virtual host is associated with one or more [[Fully Qualified Domain Name (FQDN)|domain names]] (or hostnames) and is configured to serve content and respond to requests as if it were a separate, dedicated server.

Virtual hosting is a way to efficiently use server resources and enable the hosting of multiple websites on a single server.

It allows websites with different domain names to share the same server and [[IP address]] but still have their own isolated configurations, content directories, and settings.

There are two main types of virtual hosts:

1. **Name-based Virtual Hosts**: In this approach, the web server uses the "Host" [[HTTP Headers|header]] in HTTP requests to determine which virtual host should handle the incoming request. This allows multiple domain names to share the same IP address. It's the most common method for hosting multiple websites on a single server.
2. **IP-based Virtual Hosts**: With IP-based virtual hosting, each virtual host has its own unique IP address. This means that different IP addresses are assigned to different virtual hosts, and requests to a specific IP address are directed to the corresponding virtual host. This method is less common than name-based virtual hosting and often requires additional IP addresses.
