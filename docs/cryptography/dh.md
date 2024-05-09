Diffie-Hellman is a key exchange algorithm used for securely exchanging cryptographic keys over a public channel. This method allows two parties to establish a shared secret key, which can then be used for encrypted communication. The strength of Diffie-Hellman lies in the fact that while it's relatively easy for the involved parties to agree on the shared secret, it is extremely difficult for an eavesdropper to determine the key, even if they can observe the entire key exchange process.

Both parties agree on two prime numbers. One is a large prime (p), and the other is a base (g) which is a primitive root modulo p. These numbers are public and can be known by an eavesdropper without compromising the security of the key exchange.

Each party selects a private key, which is a secret number. Each then computes their public key by raising the base (g) to the power of their private key and then taking the modulus of p (g^private_key mod p). The resulting public keys are then exchanged over the public channel.

After receiving the other party’s public key, each party raises it to the power of their own private key and again takes the modulus of p. This operation results in both parties arriving at the same number, which becomes the shared secret key.

The security of the Diffie-Hellman key exchange lies in the difficulty of the [Discrete Logarithm Problem](../cryptography/dlp.md). While it's computationally easy to raise g to a power and take a modulus p, it's hard to do the inverse — that is, to start with g^x mod p and then find x.

It’s widely used in various protocols for secure key exchange, like in [SSL/TLS](../cryptography/ssltls.md) for establishing secure web connections. When used in protocols like [TLS](../cryptography/tls.md), Diffie-Hellman can provide [[Perfect Forward Secrecy]], meaning that even if a long-term private key is compromised, session keys cannot be deduced.

Without additional authentication measures, Diffie-Hellman is vulnerable to [man-in-the-middle attacks](../security/mitm.md), where an attacker intercepts and replaces public keys. The security of Diffie-Hellman depends on using sufficiently large primes and unique private keys.
