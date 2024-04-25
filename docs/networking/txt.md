The DNS ‘text’ (TXT) record lets a domain administrator enter text into the [Domain Name System (DNS)](../networking/dns.md). The TXT record was originally intended as a place for human-readable notes.

However, now it is also possible to put some machine-readable data into TXT records. One domain can have many TXT records.

Example of a TXT record:

| example.com | record type: | value:                                            | TTL   |
| ----------- | ------------ | ------------------------------------------------- | ----- |
| @           | TXT          | This is an awesome domain! Definitely not spammy. | 32600 |

Today, two of the most important uses for DNS TXT records are email spam prevention and domain ownership verification, although TXT records were not designed for these uses originally.
