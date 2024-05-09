Perfect Forward Secrecy (PFS) is a property of secure communication protocols that ensures a session's encryption keys cannot be compromised even if the long-term secret keys used for encrypted communications are compromised in the future. PFS is crucial for maintaining the confidentiality of past communication sessions.

PFS typically involves generating a unique session key for each communication session. These keys are used for encrypting and decrypting messages during the session. PFS is often achieved through key agreement protocols like [Diffie-Hellman](../cryptography/dh.md), which allow two parties to establish a shared secret key over an open channel without the key itself ever being transmitted or exposed.

Once the communication session is over, the session keys are discarded. Without these keys, it becomes impossible to decrypt the session data, even if the attacker obtains the long-term keys.

If a server’s private key is compromised (for instance, if a hacker breaches the server or if future advances in computing make cracking the key feasible), any past communications encrypted with keys associated with that private key are still secure, as those specific session keys cannot be retroactively deciphered.

PFS adds an additional layer of security in data transmission, particularly in cases where sensitive information is being communicated over a period.

Modern implementations of [SSL/TLS](../cryptography/ssltls.md) protocols (like TLS 1.3) use PFS by default by employing ephemeral versions of key exchange algorithms (like [Diffie-Hellman Ephemeral](../cryptography/dhe.md) or DHE, and [Elliptic Curve Diffie-Hellman Ephemeral](../cryptography/ecdh.md) or ECDHE).

Implementing PFS can increase the computational load on a server since it requires generating new keys for each session. PFS doesn't protect against the disclosure of session keys that are currently in use or against the compromise of the data before encryption or after decryption.