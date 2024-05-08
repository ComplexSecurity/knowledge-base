File Transfer Protocol Secure (FTPS), also known as FTP Secure and FTP-SSL, is an extension of the standard [File Transfer Protocol](../protocols/ftp.md) (FTP). It adds support for the Transport Layer Security ([TLS](../cryptography/tls.md)) and, formerly, the Secure Sockets Layer ([SSL](../cryptography/ssl.md)) cryptographic protocols. FTPS should not be confused with [SFTP](../protocols/sftp.md) (SSH File Transfer Protocol), which is an entirely different protocol.

FTPS uses TLS (or SSL) to encrypt data sent over the network. This encryption secures the data transfer process, protecting the data from being intercepted or read by unauthorized parties. FTPS allows for the authentication of the server and, optionally, the client. This is typically done using digital certificates.

Two Modes:

- **Explicit FTPS (FTPS/E)**: The client must explicitly request security from an FTPS server and then step up to a TLS-secured connection. It's often referred to as FTPES.
- **Implicit FTPS (FTPS/I)**: A deprecated mode where TLS security is automatically initiated at the start of the connection. In this mode, an FTPS client is expected to "speak" TLS from the outset of the connection.

When an FTPS client connects to an FTPS server, they establish a control connection through which the client can send commands and receive responses. This connection can be secured using TLS/SSL. For transferring files, a separate data connection is established, which can also be secured. During the process, the server (and optionally the client) is authenticated using certificates. All commands and data are encrypted when sent over the network.

An extension of FTP with TLS for security. It uses the standard FTP protocol, securing it with TLS/SSL encryption. A different protocol built as part of SSH ([Secure Shell](../protocols/ssh.md)). SFTP provides file transfer capability as part of the SSH protocol suite, securing the file transfer by the SSH encryption and authentication mechanisms.

FTPS is used in scenarios where secure file transfer is required, such as in corporate networks, banking systems, and other areas where sensitive data is transferred. It is particularly useful in legacy systems where FTP is already in use, and an upgrade to secure file transfer is needed.

