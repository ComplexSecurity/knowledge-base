DNS AAAA records match a [Fully Qualified Domain Name (FQDN)](../web/fqdn.md) to an IPv6 address. DNS AAAA records are exactly like [DNS A Records](../networking/a.md), except that they store a domain's IPv6 address instead of its IPv4 address.

IOne of the important differences between IPv6 and IPv4 is that IPv6 addresses are longer than IPv4 addresses. The Internet is running out of IPv4 addresses, just as there are only so many possible phone numbers for a given area code. But IPv6 addresses offer exponentially more permutations and thus far more possible IP addresses.

Here is an example of an AAAA record:

| example.com | record type: | value:                                       | TTL   |
| ----------- | ------------ | -------------------------------------------- | ----- |
| @           | AAAA         | 2001:0db8:85a3:0000: <br>0000:8a2e:0370:7334 | 14400 |
