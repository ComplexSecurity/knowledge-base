Counter (CTR) mode is a mode of operation for block cipher encryption that turns a block cipher into a stream cipher. It generates the next keystream block by encrypting successive values of a "counter". The counter can be any function which produces a sequence which is guaranteed not to repeat for a long time, although an actual increment-by-one counter is the simplest and most popular.

In CTR mode, a counter, typically a simple increasing value, is encrypted to create a keystream block. This keystream is then XORed (exclusive or) with the plaintext to produce ciphertext.

Unlike traditional block modes, which encrypt block by block, CTR mode allows a block cipher to operate as a stream cipher. It encrypts individual bits/bytes of data, making it more flexible in handling data of varying lengths.

One of the advantages of CTR mode is that it allows for parallel encryption and decryption, as each block can be processed independently. This can lead to performance improvements in multi-core processors.

The counter values must be unique for each plaintext block across all messages encrypted with the same key. Typically, a nonce (number used once) is combined with a simple counter to ensure uniqueness.

In CTR mode, an error in one ciphertext block does not propagate to other blocks. This is different from modes like CBC, where an error can affect subsequent blocks.

CTR mode allows random access to the encrypted data blocks. You can decrypt any block of ciphertext without needing to process previous blocks, which is beneficial for certain applications like database encryption.

The security of CTR mode heavily depends on never using the same counter value with the same key. The unique counter and key combination ensures that the keystream is unpredictable.

CTR mode is widely used in various cryptographic protocols and applications, including AES-GCM ([[Galois Counter Mode (GCM)|Galois Counter Mode]]), which is a variant of CTR.

The simplicity of CTR mode and its ability to precompute keystream blocks make it efficient for various implementations. The nonce part of the counter must be generated in a secure manner to prevent vulnerabilities. Using a predictable nonce can severely compromise the security of the encryption.
