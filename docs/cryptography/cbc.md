Cipher Block Chaining (CBC) is a mode of operation used in block cipher encryption algorithms. In CBC mode, each block of plaintext is XORed (exclusive or) with the previous ciphertext block before being encrypted. This method of encryption provides enhanced security compared to the basic [[Electronic Codebook (ECB)]] mode.

In CBC mode, the encryption of each block of plaintext depends on the previous ciphertext block. This creates a chain of dependency among all the blocks, hence the name "**Cipher Block Chaining**."

CBC mode requires an Initialization Vector (IV) for the first block of data. The IV is a random or pseudo-random string of bits that is the same length as the block size. It ensures that the same plaintext block will encrypt to different ciphertext blocks each time, increasing security.

Before a plaintext block is encrypted, it is XORed with the preceding ciphertext block. For the first block, the IV is used for the XOR operation. Due to the chaining mechanism, an error in one ciphertext block affects the decryption of all subsequent blocks. This also means that the entire message must be received without error for proper decryption.

CBC mode provides more security than ECB mode because it obscures patterns in the plaintext. In ECB mode, identical plaintext blocks result in identical ciphertext blocks, which can reveal patterns and weaken security.

CBC mode has been widely used in various encryption protocols, including [[SSL-TLS]] for secure web communications and in standards like [[PGP (Pretty Good Privacy)]] for email encryption.

Since block ciphers require input blocks of a fixed size, plaintext often needs to be padded to the appropriate block length before encryption in CBC mode. Standard padding schemes must be used to ensure proper encryption and decryption.

Unlike some other modes, CBC encryption is not parallelizable due to the dependency of each block on the previous block. However, decryption can be performed in parallel.

While more secure than ECB, CBC mode is susceptible to certain types of cryptographic attacks, such as padding oracle attacks, especially if implemented without proper precautions. While CBC has been a popular mode of operation, newer and more secure modes like Galois/Counter Mode (GCM) are recommended for high-security applications.
