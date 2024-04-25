CMAC (Cipher-based Message Authentication Code) is a type of [[Message Authentication Code (MAC)]] that uses a block cipher to provide data integrity and authenticity assurances. Developed as a replacement for older MAC algorithms like CBC-MAC, CMAC addresses some of their limitations and provides a more secure approach for authenticating messages.

CMAC operates on block ciphers like [[Advanced Encryption Standard (AES)|AES (Advanced Encryption Standard)]] or [[Triple DES (3DES)|Triple DES]]. It uses the block cipher as a building block to create the MAC. Regardless of the size of the input data, CMAC produces a MAC of a fixed length, determined by the block size of the underlying cipher (e.g., 128 bits for AES).

CMAC provides strong security guarantees, including resistance to various cryptographic attacks such as replay and forgery attacks, when used with a secure block cipher. Like other MACs, CMAC requires a secret key shared between the sender and receiver. The MAC is generated using this key and can only be verified by someone who possesses the same key.

CMAC processes the input message in blocks. If the last block is not the size of the cipher's block size, it's padded. The algorithm maintains an internal state, which is updated with each block of the message. After processing all blocks, CMAC applies the encryption key to the final state to produce the MAC.

CMAC is used in scenarios where it's essential to verify that a message hasn't been altered and to confirm its origin. This is critical in secure communications, financial transactions, and data storage systems.

It is used in protocols like [[IPsec]] (Internet Protocol Security) and [[TLS]] (Transport Layer Security), CMAC can be used for message authentication. CMAC is often employed in custom cryptographic protocols and systems, particularly where block cipher algorithms like AES are already in use for encryption.
