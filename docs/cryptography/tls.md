TLS, or Transport Layer Security, is a cryptographic protocol designed to provide secure communication over a computer network. It is the successor to Secure Sockets Layer ([SSL](../web/ssl.md)), although the term "SSL" is still commonly used to refer to both SSL and TLS. TLS ensures privacy between communicating applications and their users on the internet, preventing eavesdropping, tampering, or message forgery.

TLS operates between the transport (e.g., [TCP](../networking/tcp.md)) and application layers (e.g., [HTTP](../web/http.md) for web browsers). The protocol works through a process that involves the following steps:

**Handshake**:

- This is the initial phase where the TLS parameters are negotiated between the client (e.g., a web browser) and the server (e.g., a web server).
- During the handshake, the server presents its TLS certificate for authentication, and the client and server agree on the version of TLS to use, select cryptographic algorithms, and optionally authenticate the client.
- They also generate shared secret keys for encrypting the data transferred in the session.

**Data Transfer**:

- Once the secure connection is established, data can be transferred between the client and server over this secure channel.
- The data is encrypted using the agreed-upon encryption standards and keys, ensuring that it remains confidential and intact during transit.

**Session Closure**:

- When the session is completed, a closure alert is sent to terminate the session, ensuring a clean shutdown of the session.

There have been several versions of TLS since its inception:

- **TLS 1.0**: Released in 1999 as an upgrade of SSL 3.0.
- **TLS 1.1**: Introduced in 2006, provided improved protection against certain types of cryptographic attacks.
- **TLS 1.2**: Released in 2008, added stronger cryptographic algorithms and better security practices.
- **TLS 1.3**: The latest version, finalized in 2018, provides improved speed and security. It simplifies the handshake process and supports modern cryptographic algorithms.

TLS ensures that data exchanged between the client and server is not readable by others. It protects data from being altered or tampered with during transmission. TLS facilitates the authentication of servers (and optionally clients), ensuring that users are communicating with legitimate entities.

Used in [HTTPS](../web/https.md), the secure version of HTTP, for secure web browsing. Used in protocols like [SMTPS](../protocols/smtps.md), [POP3S](../protocols/pops.md), and [IMAPS](../protocols/imaps.md) for secure email communication. Utilized in protocols like [FTPS](../protocols/ftps.md)  for secure file transfers.