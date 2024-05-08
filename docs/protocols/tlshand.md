The [TLS]() (Transport Layer Security) handshake is a protocol used to establish a secure communication channel between two parties — typically a web server and a client (such as a web browser). This process involves the negotiation of various parameters to create a secure connection, including authentication, cipher suite selection, and key exchange. 

The TLS handshake is more secure and is the successor to the older [SSL (Secure Sockets Layer) handshake](../web/sslhand.md). 

The handshake begins with the client sending a "Client Hello" message to the server. This message includes the TLS version the client supports, a list of supported cipher suites (encryption algorithms), and a randomly generated session key. The server responds with a "Server Hello" message, choosing a TLS version and a cipher suite from the options provided by the client. It also sends its own randomly generated session key.

The server sends its digital certificate to the client. The certificate typically includes the server's public key and is issued by a trusted [Certificate Authority (CA)](../web/cas.md). If the selected cipher suite requires additional data exchange for key generation (like in [Diffie-Hellman](../cryptography/dh.md)), the server provides the necessary parameters.

The server can optionally request a certificate from the client for mutual authentication. The "Server Hello Done" indicates the end of the server's response. If requested, the client sends its certificate to the server.

The client sends a key exchange message. This often includes a pre-master secret encrypted with the server's public key, which will be used to generate a shared session key. If the client sent a certificate, it also sends a message signed with its private key, proving it owns the sent certificate.

Both the client and server send a "Change Cipher Spec" message, signalling that subsequent messages will be encrypted using the agreed cipher suite and keys. Both parties exchange encrypted "Finished" messages, verifying that the handshake has been completed successfully.

After the handshake, a secure communication channel is established. All data transmitted between the client and server is encrypted with the session keys derived during the handshake.

