Rijndael is a symmetric key encryption algorithm that was selected as the [[Advanced Encryption Standard (AES)]] by the U.S. National Institute of Standards and Technology (NIST) in 2001.

Rijndael is a block cipher, meaning it encrypts data in fixed-size blocks. The standard block size is 128 bits, but Rijndael can be implemented with block sizes of 192 or 256 bits as well. It uses the same key for both encryption and decryption. Key sizes can be 128, 192, or 256 bits, offering a good balance between security and performance.

AES is widely regarded as highly secure and is used globally for various security applications. Its adoption as a standard reflects its strength and the confidence of the cryptographic community in its security properties. 

Rijndael/AES is efficient in both software and hardware implementations, making it suitable for a wide range of applications, from high-end servers to small embedded devices. While AES itself is a block cipher, it can be used in different modes of operation (like [[Cipher Block Chaining (CBC)|CBC]], [[Galois Counter Mode (GCM)|GCM]], [[Counter (CTR)|CTR]]) to encrypt data streams of arbitrary length or to provide additional security features.

AES is used in [[SSL-TLS|SSL/TLS]] for secure web communications, [[Virtual Private Network|VPNs]], and many other types of secure data transmission. It's used in various file and disk encryption systems to protect data at rest. Given its security, AES is used in sensitive government and military communications. AES is also used in cryptocurrency wallets and blockchain technologies for securing transactions.

Here's a conceptual example of using AES in a programming context:

```python
# Pseudo-code example
from Crypto.Cipher import AES

key = generate_aes_key()  # Generate a secure AES key
cipher = AES.new(key, AES.MODE_CBC)  # Create a new AES cipher

# Encrypting data
plaintext = "Secret Data"
ciphertext = cipher.encrypt(pad(plaintext, AES.block_size))

# Decrypting data
decrypted = unpad(cipher.decrypt(ciphertext), AES.block_size)
```

While AES is based on Rijndael, the term "AES" specifically refers to the standard adopted by NIST, which uses the Rijndael algorithm with a fixed block size of 128 bits and key sizes of 128, 192, or 256 bits. The original Rijndael algorithm was designed to be more flexible with both block and key sizes, but this flexibility is not part of the AES standard.