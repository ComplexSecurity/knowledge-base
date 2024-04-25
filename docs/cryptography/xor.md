XOR, or exclusive OR, is a logical bitwise operator that compares two binary inputs; it outputs true (or 1) only when the inputs are different. In the context of binary numbers, XOR compares each bit of two values and returns 1 if the bits are different and 0 if they are the same.

For two inputs, A and B, the XOR operation can be represented as follows:

- A XOR B = 1 if A ≠ B
- A XOR B = 0 if A = B

XOR is often used in encryption algorithms. One simple form is XOR cipher, where a key is applied to plaintext using the XOR operation. The same key is used to decrypt the ciphertext by XORing it again with the key.

- Example: `plaintext XOR key = ciphertext`, and then `ciphertext XOR key = plaintext`.
- This is effective when the key is random, used only once (one-time pad), and is as long as the plaintext.

In software, XOR is used to [[Obfuscation (KB)|obfuscate]] code or data to hide its purpose or content from users or analysis tools. This can protect software from reverse engineering. XOR is a fundamental operation in many cryptographic hash functions, contributing to their ability to create a unique hash value from input data.

XOR is used in some algorithms for generating pseudo-random numbers, which are important in various cryptographic applications.
