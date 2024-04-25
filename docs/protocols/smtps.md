Simple Mail Transfer Protocol Secure (SMTPS) refers to the use of [[Simple Mail Transfer Protocol]] (SMTP) over a secure connection, typically using [[SSL]] (Secure Sockets Layer) or [[TLS]] (Transport Layer Security). 

SMTP is the standard protocol for sending emails across the Internet. When SMTP is secured with SSL/TLS, it becomes SMTPS, ensuring that the email messages are transmitted in an encrypted form, providing confidentiality and data integrity between the email client and the mail server.

SMTPS encrypts the data being transmitted, which includes the email content, headers, and any authentication credentials. This prevents unauthorized interception and reading of email data during transmission. In addition to encryption, SMTPS also provides a means of authenticating the mail server, which can help prevent [[Man-in-the-Middle (MitM) attack]].

The standard port for SMTP is 25. However, for SMTPS, the commonly used port is 465. Some servers also use port 587 for SMTP with [[STARTTLS]], which upgrades a plain SMTP connection to a secure one.

When an email client sends an email using SMTPS, it first establishes a secure connection with the SMTP server using SSL/TLS. This ensures that all subsequent data exchange during the session is encrypted. Once the secure connection is established, the email client sends the email to the server using the SMTP protocol, but now over the encrypted channel.

SMTPS can also be used for encrypting emails sent between email servers. However, this is not as commonly implemented as client-to-server encryption.

The differences between SMTPS and STARTTLS are:

- **SMTPS (Implicit SSL/TLS)**: SMTPS starts with a secure connection right from the beginning. The use of SSL/TLS is implied and is a fundamental part of the connection from the start.
- **STARTTLS (Explicit SSL/TLS)**: This is an extension to plain SMTP. The email client and server start with a plain, unencrypted SMTP connection and then use the STARTTLS command to upgrade to a secure connection.

SMTPS protects the contents of emails from being intercepted and read by unauthorized parties. It also ensures that the emails are not tampered with during transit. By using SSL/TLS, SMTPS can authenticate the email servers, adding an additional layer of security.