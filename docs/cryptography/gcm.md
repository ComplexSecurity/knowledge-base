Galois/Counter Mode (GCM) is an encryption mode that combines the [[Counter (CTR)|counter mode (CTR)]] of block cipher encryption with the Galois mode of authentication. It's widely used for its efficiency and security, particularly in encrypting and authenticating data in communication protocols like TLS and [[IPsec]]. 

GCM is a mode of operation for symmetric key cryptographic block ciphers such as [[Advanced Encryption Standard (AES)|AES]]. GCM combines the counter mode (CTR) for encryption, which turns a block cipher into a stream cipher, with a Galois field multiplication operation to provide data authenticity (integrity checking).

One of the significant advantages of GCM is that it provides both confidentiality (encryption) and integrity/authentication in a single, efficient process.

GCM is known for its high performance and efficiency, particularly in hardware implementations. It can process large amounts of data quickly, making it suitable for high-speed communication channels.

GCM is used in various secure communication protocols, including TLS (Transport Layer Security) and IPsec (Internet Protocol Security), to provide secure data transmission.

GCM provides protection against replay attacks, where an adversary attempts to disrupt communication by repeating or delaying data packets. GCM requires a unique nonce (number used once) for each encryption operation with the same key. Nonce reuse can severely compromise security, particularly the confidentiality of the data.

In GCM, the counter mode operates as a stream cipher. It generates keystream blocks, which are XORed with the plaintext blocks for encryption. GCM produces an authentication tag as part of the encryption process, which can be used to verify the integrity and authenticity of the data upon decryption.


