ElGamal is a cryptographic algorithm used for both encryption and digital signatures. It's based on the [[Diffie-Hellman]] key exchange and the [[Discrete Logarithm Problem]], making it part of the family of public key cryptographic systems. ElGamal was introduced by Taher Elgamal in 1985 and remains relevant due to its security properties and its basis in mathematical problems for which no efficient solving algorithm is known.

The ElGamal encryption system is an asymmetric key encryption algorithm for public-key cryptography which is based on the Diffie-Hellman key exchange.

Like other public-key systems, ElGamal uses two keys: a public key, which can be shared openly, and a private key, which must be kept secret. It involves choosing a large prime number $p$, a generator $g$ of the multiplicative group of integers modulo $p$, and a private key $x$ which is a random number. The public key $u$ is then calculated as $y$=$g$$^x$ mod  $p$.

The encryption process is:

1. The sender, who knows the receiver's public key $y$, picks a random number $k$ and computes the shared secret $s$=$y$$^k$ mod  $p$
2. The sender then encrypts the message $m$ by multiplying it with $s$ and sends both $g$$^k$ mod $p$ and the encrypted message.

The decryption process is:

1. The receiver uses their private key $x$ and the received $g$$^k$ mod  $p$ to reconstruct the shared secret $s$ and then decrypts the message.

ElGamal can also be used for digital signatures. Its signature scheme is based on the difficulty of computing discrete logarithms.

#### Signature Generation

1. A hash or digest of the message is created.
2. The signer then uses their private key to generate a signature on the message hash.

#### Signature Verification

1. Anyone with the signer's public key can verify the authenticity of the signature by relating it to the hash of the original message.

The security of ElGamal encryption depends on the difficulty of solving the discrete logarithm problem. ElGamal is generally slower than some other public-key algorithms and generates larger ciphertexts, making it less efficient for encrypting large messages. However, it's often used for securely transmitting keys rather than the message content itself.

ElGamal encryption is used in various cryptographic applications, including secure email communication, digital signatures in software distribution, and more.
