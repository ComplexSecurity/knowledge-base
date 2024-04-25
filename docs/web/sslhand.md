The [[SSL]] (Secure Sockets Layer) Handshake is a process that occurs at the beginning of an [[SSL-TLS|SSL/TLS]] session, which is used for secure communications over the internet. It's an integral part of establishing an SSL/TLS connection, and it involves several steps to authenticate the server (and optionally the client), as well as to negotiate the encryption algorithms and keys that will be used for the session.

The handshake begins with the client (typically a web browser) sending a "Client Hello" message to the server. This message includes the client's SSL/TLS version, the list of supported cipher suites (encryption algorithms), and a randomly generated session key. In response, the server sends a "Server Hello" message, containing its SSL/TLS version, the cipher suite selected from the client's list, and its own randomly generated session key.

The server then provides its [[SSL certificates|SSL Certificate]], which includes its public key. If the server requires client authentication, it will request the client's certificate. The client verifies the server's SSL certificate against a list of trusted [[Certificate Authorities (CAs)]]. It checks whether the certificate is valid, has not expired, and is being used by the website for which it has been issued.

The client uses the public key from the server's certificate to encrypt a pre-master secret and sends it to the server. Both the client and server use the pre-master secret to generate a common session key. The server sends a "Finished" message, which is encrypted with the session key, indicating that the server part of the handshake is complete.

The client sends its own "Finished" message, also encrypted, to the server.

After the handshake, both the client and server have verified each other’s identities (in case of mutual authentication) and agreed upon encryption methods and keys. All data transmitted between the client and server is encrypted with the session key, ensuring secure communication.

Though often referred to as the SSL Handshake, SSL is an older protocol and has largely been replaced by [[TLS]] (Transport Layer Security), which is more secure. The [[TLS Handshake]] follows a similar process but includes additional security enhancements.

The handshake is crucial for setting up a secure session. It ensures that the data exchanged between client and server is encrypted and secure from eavesdropping or tampering. It also serves to authenticate the server (and optionally the client), reducing the risk of [[Man-in-the-Middle (MitM) attack|man-in-the-middle attacks]].