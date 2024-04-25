Diffie-Hellman Ephemeral (DHE) is a variation of the [[Diffie-Hellman]] key exchange protocol that provides [[Perfect Forward Secrecy|Perfect Forward Secrecy (PFS)]]. In this context, "ephemeral" refers to the short-lived nature of the keys used in the key exchange process. Unlike the basic Diffie-Hellman algorithm, which can use fixed keys, DHE generates new, temporary keys for each session.

In DHE, both parties involved in the communication generate temporary, or "ephemeral," keys for each session. These keys are used only once and then discarded.

The client and server each send their respective ephemeral public keys to the other party. As in standard Diffie-Hellman, they then use their private keys and the received public key to generate a shared secret, which is used to derive the session key for encryption.

Data transmitted during the session is encrypted using the session key. After the session ends, the ephemeral keys are discarded.

The primary advantage of using DHE is PFS. Even if a server’s long-term private key is compromised, past communication sessions remain secure since the session keys, generated uniquely for each session, cannot be retroactively deciphered. DHE adds an extra layer of security in communication protocols, making it more difficult for attackers to decrypt intercepted data.

DHE is commonly used in [[TLS]] (Transport Layer Security) and [[SSL]] (Secure Sockets Layer) protocols. When you see "DHE" as part of a cipher suite in [[SSL-TLS|SSL/TLS]], it indicates that the connection uses Diffie-Hellman Ephemeral for key exchange.

The process of generating ephemeral keys for each session can be more computationally intensive than using fixed keys. Proper implementation and configuration are crucial for ensuring the security benefits of DHE. Older or improperly configured systems may not support or optimally use DHE.
