Asymmetric encryption, also known as public key cryptography, is a method of encrypting data using a pair of keys: a public key and a private key. This cryptographic system is distinct for its use of two separate keys, in contrast to symmetric encryption which uses the same key for both encryption and decryption.

The process begins with the generation of a pair of keys. The public key, as the name suggests, can be shared with anyone, while the private key is kept secret by the owner. 

When someone wants to send a secure message, they encrypt it using the recipient's public key. This encrypted data can only be decrypted by the corresponding private key. Upon receiving the encrypted message, the recipient uses their private key to decrypt it. Since the private key is not shared, only the intended recipient can decrypt the message.

The strength of asymmetric encryption lies in the difficulty of deriving the private key from the public key. This is usually based on complex mathematical problems, such as the factoring of large numbers in [RSA (Rivest-Shamir-Adleman)](../cryptography/rsa.md) encryption.

Asymmetric encryption is widely used for secure data transmission over the internet. It’s fundamental for technologies like SSL/TLS in securing online communications, as well as in digital signatures which verify the authenticity and integrity of data.

The key advantage of asymmetric encryption is the security it provides in open networks like the internet, where exchanging secret keys (as required in [symmetric encryption](../cryptography/symmetric.md)) is not always safe or practical. 

However, it's generally slower than symmetric encryption due to its computational complexity, which is why in practice, often a combination of both methods is used (e.g., using asymmetric encryption to exchange a symmetric key safely).