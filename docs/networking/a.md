An A record maps a [Fully Qualified Domain Name (FQDN)](../web/fqdn.md) to the physical [IP address](../networking/ipa.md) of the computer hosting that domain. Internet traffic uses the A record to find the computer hosting your domain's [DNS](../networking/dns.md) settings. The value of an A record is always an IP address, and multiple A records can be configured for one domain name.

A records only hold IPv4 addresses. If a website has an IPv6 address, it will instead use an [DNS AAAA Record](../networking/aaaa.md)

Here is an example of an A record:

| example.com | record type: | value:    | TTL   |
| ----------- | ------------ | --------- | ----- |
| @           | A            | 192.0.2.1 | 14400 |

The "@" symbol in this example indicates that this is a record for the root domain, and the "14400" value is the TTL (time to live), listed in seconds. The default TTL for A records is 14,400 seconds. This means that if an A record gets updated, it takes 240 minutes (14,400 seconds) to take effect.
