A "canonical name" (CNAME) record points from an alias domain to a "canonical" domain. A CNAME record is used in lieu of an [DNS A Records](a.md), when a domain or subdomain is an alias of another domain. 

All CNAME records must point to a domain, never to an [IP address](ip.md). Imagine a scavenger hunt where each clue points to another clue, and the final clue points to the treasure. 

A domain with a CNAME record is like a clue that can point you to another clue (another domain with a CNAME record) or to the treasure (a domain with an A record).

For example, suppose blog.example.com has a CNAME record with a value of "example.com" (without the "blog"). This means when a DNS server hits the DNS records for blog.example.com, it actually triggers another DNS lookup to example.com, returning example.com’s IP address via its A record. 

In this case we would say that example.com is the canonical name (or true name) of blog.example.com.

Oftentimes, when sites have subdomains such as blog.example.com or shop.example.com, those subdomains will have CNAME records that point to a root domain (example.com). 

This way if the IP address of the host changes, only the DNS A record for the root domain needs to be updated and all the CNAME records will follow along with whatever changes are made to the root.

A frequent misconception is that a CNAME record must always resolve to the same website as the domain it points to, but this is not the case. The CNAME record only points the client to the same IP address as the root domain. 

Once the client hits that IP address, the web server will still handle the URL accordingly. So for instance, blog.example.com might have a CNAME that points to example.com, directing the client to example.com’s IP address. 

But when the client actually connects to that IP address, the web server will look at the URL, see that it is blog.example.com, and deliver the blog page rather than the home page.

Example of a CNAME record:

|blog.example.com|record type:|value:|TTL|
|---|---|---|---|
|@|CNAME|is an alias of example.com|32600|

