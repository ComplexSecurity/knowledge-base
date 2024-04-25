Internet Message Access Protocol Secure (IMAPS) refers to the use of the [[Internet Message Access Protocol]] (IMAP) over an encrypted connection. IMAP is a standard email retrieval protocol used to access and manage a user's email on a mail server, and when it's used in conjunction with security protocols like [[TLS]] (Transport Layer Security) or [[SSL]] (Secure Sockets Layer), it becomes IMAPS.

IMAPS uses SSL/TLS to encrypt the connection between the email client and the email server. This ensures that all communication, including email messages, login credentials, and other transmitted data, is secure and cannot be easily intercepted or read by unauthorized parties. 

While standard IMAP typically uses port 143, IMAPS usually operates over port 993. Using a designated port helps in managing and securing network traffic more effectively. In addition to encrypting data, SSL/TLS also authenticates the mail server to the email client, helping to prevent [[Man-in-the-Middle (MitM) attack|man-in-the-middle attacks]].

When an email client connects to an email server using IMAPS, it initiates a secure connection using SSL/TLS. Once the secure connection is established, the client and server exchange data securely. The client can then retrieve, read, delete, or move emails, or mark them as read/unread, all while ensuring that the data remains encrypted during transit between the server and the client.

IMAPS is often compared with [[Post Office Protocol Secure|POP3S]] (Post Office Protocol version 3 Secure), another protocol used for retrieving emails securely. The main difference lies in how they handle emails:

- **IMAP/IMAPS**: Allows users to view and manage emails directly on the server. Changes made in the email client are reflected on the server, making IMAP suitable for accessing email from multiple devices.
- **POP3/POP3S**: Designed to download emails from the server to the client. Once downloaded, emails are typically deleted from the server.

It encrypts the data protects against eavesdropping and ensures the confidentiality and integrity of the email communication. IMAP allows users to manage their emails directly on the server, which is convenient for users who access their emails from multiple devices.

