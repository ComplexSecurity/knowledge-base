A Mail Transport Agent (MTA), also known as a mail relay or mail server, is a software application that transports emails from one computer to another using the [[Simple Mail Transfer Protocol]] (SMTP). 

It is a critical component of the internet's email infrastructure, responsible for transferring email messages from the sender's to the recipient's mail server, and often to the recipient's local [[Mail User Agent (MUA)|mail user agent (MUA)]], which is the email client.

MTAs determine the route and deliver emails across the internet or within an organization. They use SMTP to communicate with other MTAs and with MUAs. If an MTA cannot immediately deliver an email (e.g., if the recipient's server is down), it queues the email and periodically retries delivery.

MTAs often process email by performing tasks like adding headers, filtering spam, or scanning for viruses. MTAs relay emails from one MTA to another until the email reaches its final destination.

Some common MTA software applications include:

- [[Sendmail]]: One of the oldest and most widely used MTAs on Unix-like systems.
- [[Postfix]]: Known for its easy configuration and secure default settings, Postfix is widely used in Linux environments.
- [[Exim]]: Popular on Unix-like systems, Exim is known for its flexibility and configurability.
- [[Microsoft Exchange Server]]: Widely used in corporate environments, particularly in organizations using Microsoft infrastructure.

When you send an email, your email client (MUA) submits the email to an MTA. This submission usually uses SMTP or submission protocols (like [[Simple Mail Transfer Protocol Secure (SMTPS)|SMTPS]] or SMTP over [[STARTTLS]]). The MTA then relays the email through potentially several other MTAs until it reaches the MTA responsible for the recipient's domain. Finally, that MTA delivers the email to the recipient's mailbox, where it can be accessed by their email client.



