The [DNS](../networking/dns.md) ‘start of authority’ (SOA) record stores important information about a domain or zone such as the email address of the administrator, when the domain was last updated, and how long the server should wait between refreshes.

All DNS zones need an SOA record in order to conform to IETF standards. SOA records are also important for zone transfers.

Example of an SOA record:

|             |                      |
| ----------- | -------------------- |
| name        | example.com          |
| record type | SOA                  |
| MNAME       | ns.primaryserver.com |
| RNAME       | admin.example.com    |
| SERIAL      | 1111111111           |
| REFRESH     | 86400                |
| RETRY       | 7200                 |
| EXPIRE      | 4000000              |
| TTL         | 11200                |

The 'RNAME' value here represents the administrator's email address, which can be confusing because it is missing the ‘@’ sign, but in an SOA record admin.example.com is the equivalent of admin\@example.com.
