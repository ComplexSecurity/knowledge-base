GMAC (Galois/Counter Mode MAC) is a type of [[Message Authentication Code (MAC)]] used in cryptographic communications. It is specifically associated with [[Galois Counter Mode (GCM)|Galois/Counter Mode (GCM)]], which is a mode of operation for symmetric key cryptographic block ciphers. GMAC provides a way to ensure both the integrity and authenticity of a message.

GMAC is often used in conjunction with Galois/Counter Mode, a mode that combines the counter mode of encryption with the Galois mode of authentication. The GCM, which includes GMAC, is used for encrypting and authenticating data.

It operates within the realm of symmetric key encryption, meaning the same key is used for both encryption and decryption. GMAC (and GCM) is designed to provide high-performance authenticated encryption and is particularly efficient for hardware implementations. It is highly secure and resistant to various cryptographic attacks when used correctly.

GMAC is typically used with block ciphers like [[Advanced Encryption Standard (AES)|AES (Advanced Encryption Standard)]]. In GCM, the block cipher operates in counter mode for encryption, while GMAC provides message authentication.

In GCM, data is encrypted in a stream cipher mode (using the counter mode of encryption) and authenticated using GMAC. GMAC generates an authentication tag (MAC) for a message and a nonce (number used once). This tag is used to verify the integrity and authenticity of the message at the receiving end. A unique nonce is used for each message to ensure the security of the encryption and authentication process.

GMAC is widely used in secure communication protocols, especially where high throughput and strong security are required. It's used in protocols like [[TLS]] (Transport Layer Security) and [[IPsec]] (Internet Protocol Security).

Given its efficiency, GMAC is suitable for environments with limited computational resources, such as wireless and mobile applications.