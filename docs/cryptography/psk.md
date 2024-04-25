A pre-shared key (PSK) is a secret key used in cryptography that is shared between two parties before being used in a security protocol, such as an encryption or authentication process. PSK is commonly used in various network security contexts, including Wi-Fi networks and [[Virtual Private Network|VPNs]].

The key must be shared between parties before it can be used for secure communication. This sharing is typically done over a secure channel or through a secure method of distribution.

PSKs are used in [[Symmetric Encryption|symmetric key cryptography]], where the same key is used for both encryption and decryption of messages. In Wi-Fi networks, a PSK is often used in [[WPA (Wi-Fi Protected Access)|WPA]] and [[WPA2]] (Wi-Fi Protected Access) security protocols. The PSK is what is commonly referred to as the "Wi-Fi password".

PSKs are relatively simple to implement compared to more complex key management systems. They don't require a certificate infrastructure or extensive authentication processes. In VPNs (Virtual Private Networks), PSKs can be used to authenticate the endpoints of the VPN connection. Each endpoint must know the PSK to establish a secure connection.

The strength of a PSK-based system depends on the secrecy and randomness of the key. A weak or compromised PSK can lead to security vulnerabilities. PSK systems can become cumbersome in large-scale environments because the key must be securely distributed to each party and maintained. This can become a logistical challenge as the number of users increases.

In [[IPsec]] protocols, PSKs are one method of establishing the identity of the communicating parties, especially in [[Internet Key Exchange (IKE)|IKE (Internet Key Exchange)]] to set up secure IPsec connections. If a PSK is exposed, all data previously transmitted using that key can potentially be decrypted, assuming an attacker has access to the encrypted data.

