A key exchange in the context of web communication refers to the process of exchanging cryptographic keys between a [[Client|client]] and a [[Server|server]] during the establishment of a secure [[HTTPS Protocol|HTTPS]] connection.

This key exchange is a crucial part of the SSL/TLS (Secure Socket Layer/Transport Layer Security) protocol, which ensures secure communication over the internet.

The key exchange process typically involves the following steps:

1. **Initiation**: When you connect to a secure website (one using HTTPS), your browser sends a 'ClientHello' message to the server, indicating its SSL/TLS capabilities
2. **Server Response**: The server replies with a 'ServerHello' message, agreeing on the SSL/TLS version and cryptographic methods to use. The server also sends its digital certificate, which contains the server's public key
3. **Key Exchange**: The browser verifies the server's certificate (to ensure it's trustworthy) and then uses the server's public key to encrypt a pre-master secret. This encrypted secret is sent to the server.
4. **Secret Derivation**: Both the server and the browser independently use this pre-master secret to generate a common 'master secret'. From this master secret, they both derive a set of symmetric encryption keys.
5. **Encrypted Communication**: All further communication in this session is encrypted using the symmetric keys, ensuring that the data exchanged between the browser and the server is secure and private.