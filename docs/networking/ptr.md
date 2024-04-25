A DNS PTR (Pointer) record is a type of [DNS](../networking/dns.md) record used for reverse DNS lookups. While most DNS records map domain names to [IP addresses](../networking/ipa.md) (forward DNS lookups), PTR records do the opposite; they map IP addresses to domain names (reverse DNS lookups).

While DNS A records are stored under the given domain name, DNS PTR records are stored under the IP address — reversed, and with ".in-addr.arpa" added. For example, the PTR record for the IP address 192.0.2.255 would be stored under "255.2.0.192.in-addr.arpa".

"in-addr.arpa" has to be added because PTR records are stored within the .arpa top-level domain in the DNS. .arpa is a domain used mostly for managing network infrastructure, and it was the first top-level domain name defined for the Internet.

in-addr.arpa is the namespace within .arpa for reverse DNS lookups in IPv4.
