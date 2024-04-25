A Message Authentication Code (MAC) is a short piece of information used to authenticate a message and to provide integrity and authenticity assurances on the message. A MAC function, like a cryptographic hash function, takes a secret key and an input (or message) and produces a MAC (sometimes known as a tag), which can be appended to the message and then sent to a receiver.

MACs ensure that a message comes from the stated sender (authentication) and has not been changed in transit (integrity). Unlike a hash function, a MAC function requires a secret key in addition to the message. The same key is used to generate and to verify the MAC.

Any change to the message or the MAC will make the verification fail at the receiver's end, which means any tampering with the message can be reliably detected. Common MAC algorithms include [[HMAC (Hash-based Message Authentication Code)]], [[CMAC (Cipher-based MAC)]], and [[GMAC (Galois Counter Mode MAC)]].

The sender uses a MAC algorithm, a secret key, and the message to generate a MAC. The MAC is then sent along with the message. The receiver, who has the same secret key, uses it and the received message to generate a new MAC. The receiver compares this new MAC against the MAC sent with the message. If they match, the message is authenticated and considered untampered.

MACs are used for integrity and authenticity between parties that share a secret key. They don't provide non-repudiation since both parties can generate the MAC. Digital Signatures provide integrity, authenticity, and non-repudiation, as they use public-key cryptography where the ability to generate a signature is not shared.

