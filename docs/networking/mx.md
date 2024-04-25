A [DNS](../networking/dns.md) 'mail exchange' (MX) record directs email to a mail server. The MX record indicates how email messages should be routed in accordance with the [Simple Mail Transfer Protocol](../protocols/smtp.md) (the standard protocol for all email). Like [DNS CNAME Records](../networking/cname.md), an MX record must always point to another domain.

Example of an MX record:

| example.com | record type: | priority: | value:                | TTL   |
| ----------- | ------------ | --------- | --------------------- | ----- |
| @           | MX           | 10        | mailhost1.example.com | 45000 |
| @           | MX           | 20        | mailhost2.example.com | 45000 |

The 'priority' numbers before the domains for these MX records indicate preference; the lower 'priority' value is preferred. The server will always try mailhost1 first because 10 is lower than 20. In the result of a message send failure, the server will default to mailhost2.

The email service could also configure this MX record so that both servers have equal priority and receive an equal amount of mail:

| example.com | record type: | priority: | value:                | TTL   |
| ----------- | ------------ | --------- | --------------------- | ----- |
| @           | MX           | 10        | mailhost1.example.com | 45000 |
| @           | MX           | 10        | mailhost2.example.com | 45000 |

This configuration enables the email provider to equally balance the load between the two servers.
