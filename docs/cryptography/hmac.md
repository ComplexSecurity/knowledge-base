HMAC (Hash-based Message Authentication Code) is a type of cryptographic function used to create a [message authentication code (MAC)](../misc/mac.md) involving a cryptographic hash function in combination with a secret cryptographic key. It provides both integrity and authentication of a message. HMAC is widely used in various security applications and protocols, including [TLS](../cryptography/tls.md) and [SSL](../cryptography/ssl.md), [IPsec](../protocols/ipsec.md), and more.

HMAC combines a user-provided secret key with the data/message to be authenticated. The key is used in conjunction with the hash function to create a unique MAC for the data. A cryptographic hash function (like [SHA-256](../cryptography/sha256.md)) is used to compute the hash. This function takes an input (or 'message') and returns a fixed-size string of bytes. The output is typically a hash value or digest.

The process is as follows:

- The key is combined with the input message.
- The combined key and message are then passed through the hash function.
- The output hash (MAC) is then used to verify the integrity and authenticity of the message.

To verify the message, the receiver uses the same key and hash function to generate an HMAC from the received message. If this HMAC matches the one sent with the message, it confirms that the message has not been altered and is authentic.

HMAC provides security against certain types of cryptographic attacks (like [collision attacks](../security/coll.md)) inherent in traditional hash functions when used for MAC purposes. The security of an HMAC depends on the secrecy of the key; as long as the key is kept secret, it is very difficult to forge a MAC.

HMAC can be used with any cryptographic hash function, like [MD5](../cryptography/md5.md) or [SHA-256](../cryptography/sha256.md) with the security strength being contingent upon the underlying hash function.

It is commonly used for the following:

- **Data Integrity**: Ensuring that data has not been altered during transmission.
- **Authentication**: Verifying that a message was sent by the holder of the secret key.
- **Secure Communications**: Used in various network security protocols (like [SSL/TLS](../cryptography/ssltls.md)) for secure data transmission.
- **API Security**: Often used to authenticate API requests between a client and a server.