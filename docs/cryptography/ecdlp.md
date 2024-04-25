The Elliptic Curve Discrete Logarithm Problem (ECDLP) is a mathematical problem that serves as the foundation for [[elliptic curve cryptography (ECC)]], a form of public key cryptography. Similar to the [[Discrete Logarithm Problem|discrete logarithm problem (DLP)]] in its traditional form, ECDLP is considered hard to solve, which is what makes it useful for cryptographic purposes.

The main difference lies in the mathematical structure used: ECDLP is based on the arithmetic of elliptic curves, whereas traditional DLP relies on the arithmetic of finite fields.

In the context of elliptic curves, the ECDLP can be described as follows:

- Given an elliptic curve $E$ over a finite field, a point $P$ on $E$, and another point $Q$ on $E$, the Elliptic Curve Discrete Logarithm Problem is to find an integer $k$, if it exists, such that $Q$ = $k$$P$. Here, $P$ and $Q$ are known, and the goal is to determine $k$.

The ECDLP is believed to be much more difficult to solve than the traditional discrete logarithm problem for a given key size, providing higher security with smaller key sizes. Due to the increased difficulty of ECDLP, elliptic curve cryptography can achieve comparable levels of security to other public key systems like [[RSA (Rivest-Shamir-Adleman)|RSA]] but with much smaller keys. Smaller keys mean less computational overhead, leading to faster processing and lower energy consumption.

ECC, and thus ECDLP, is used in a variety of cryptographic applications, including encryption, digital signatures, and key agreement protocols. It's widely used in mobile and wireless devices due to its efficiency.

The assumption that ECDLP is hard to solve underpins the security of ECC. If an efficient solution to ECDLP were found, it would compromise the security of all cryptographic systems based on ECC.

Due to its efficiency and strong security, ECC has seen widespread adoption, especially in areas where computational resources are limited or where high performance is required, such as in IoT devices, smartphones, and secure web communications ([[TLS]]/[[SSL]]).
