AES-GCM, or Advanced Encryption Standard in Galois/Counter Mode, is a cryptographic mode of operation that provides both confidentiality (encryption) and data integrity (authentication). It combines the [[Advanced Encryption Standard (AES)|AES]] block cipher with a mode of operation called [[Galois Counter Mode (GCM)|Galois/Counter Mode (GCM)]]. AES-GCM is widely used because of its efficiency and security, and it is one of the standard modes recommended by various cryptographic organizations and standards.

AES-GCM performs both encryption and authentication in a single step, providing efficient and secure protection of data. It uses AES in counter mode for encryption, which turns AES into a stream cipher. This mode encrypts plaintext blocks by combining them with an encrypted counter block.

The Galois mode provides message authentication using a mechanism known as [[GMAC (Galois Counter Mode MAC)|GMAC (Galois Message Authentication Code)]]. It ensures data integrity and authenticity. AES-GCM requires a unique nonce (number used once) for each encryption operation with the same key. The nonce ensures that the same plaintext encrypts differently each time, enhancing security.

AES-GCM is efficient in both hardware and software implementations. It's particularly well-suited for high-throughput, low-latency applications. Since it operates in a stream cipher mode, AES-GCM doesn't require padding of the plaintext to a multiple of the block size.

Widely used in [[TLS]] (Transport Layer Security) and [[Virtual Private Network|VPNs]] (Virtual Private Networks) for securing internet traffic. It is used for encrypting sensitive data both in transit and at rest, such as in disk encryption or database encryption. AES-GCM's authentication capability ensures that data has not been tampered with, making it suitable for scenarios where data integrity is critical.

In a programming context, using AES-GCM might look like this:

```python
# Pseudo-code example
from Crypto.Cipher import AES
from Crypto.Random import get_random_bytes

key = get_random_bytes(16)  # AES key
nonce = get_random_bytes(12)  # Unique nonce for each encryption

# Creating AES-GCM cipher
cipher = AES.new(key, AES.MODE_GCM, nonce=nonce)

# Encrypting data
plaintext = "Sensitive data"
ciphertext, tag = cipher.encrypt_and_digest(plaintext)

# Decrypting data (in a separate process with the same key and nonce)
decryptor = AES.new(key, AES.MODE_GCM, nonce=nonce)
decrypted_text = decryptor.decrypt_and_verify(ciphertext, tag)
```

It's crucial to use a unique nonce for each encryption with the same key. Nonce reuse in AES-GCM can significantly compromise security, particularly revealing information about the plaintext and authentication keys. As with any encryption standard, secure key management practices are essential to maintain the overall security of the system.