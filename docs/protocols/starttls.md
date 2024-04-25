STARTTLS is a protocol command used to upgrade a plain text connection to a secure ([[TLS]] or [[SSL]]) connection rather than using a separate port for encrypted communication. It's an extension to the communication protocols [[Simple Mail Transfer Protocol|SMTP]], [[Internet Message Access Protocol|IMAP]], and [[Post Office Protocol|POP3]], allowing these protocols to be used both in their regular, non-encrypted form and their secure, encrypted form.

The client connects to the server using a standard, non-encrypted connection (such as SMTP on port 25 for email). If both the client and server support TLS, the client sends the STARTTLS command.

The server responds, and a TLS handshake is initiated. During this handshake, the client and server agree on encryption methods and exchange keys for encrypting the session. After the handshake, the connection is encrypted, and the client and server can securely exchange data.

STARTTLS allows the use of the same port for both encrypted and non-encrypted traffic, simplifying network configurations and supporting backward compatibility. It provides a way to encrypt data transmissions without the need for a separate secure port.

STARTTLS is often described as providing opportunistic encryption, meaning that the encryption is used if both sides support it, but the connection can fall back to plain text if not. This can be a vulnerability if a [[Man-in-the-Middle (MitM) attack|man-in-the-middle attack]] is used to strip out the STARTTLS command (a form of downgrade attack).

Proper implementation and certificate validation are crucial. Clients should verify server certificates to prevent man-in-the-middle attacks.

While SMTPS (or using SMTP over SSL/TLS on a separate port) always creates a secure connection from the start, STARTTLS begins with an unencrypted connection and upgrades to encryption if possible. STARTTLS offers more flexibility and can help in environments where secure ports are blocked or not available, but it can be more susceptible to certain types of attacks if not properly configured and enforced.

