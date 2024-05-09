The Discrete Logarithm Problem (DLP) is a mathematical problem that forms the basis of certain types of cryptographic algorithms, particularly those used in asymmetric key cryptography. It is considered a "hard" problem in computational mathematics, meaning that no efficient method is currently known for solving it in all cases, especially for large numbers. This difficulty is what makes it useful for cryptography.

The problem can be stated as follows: Given a prime number $p$, a generator $g$ (a number less than $p$ that has certain properties), and a number $p$ which is a result of raising $g$ to some power $x$ modulo $p$ (i.e., $y$=$g$$^x$ mod  $p$), find the value of $x$. In other words, given $g$, $y$, and $p$, find $x$ in the equation:

- $g$$^x$ = $y$ (mod  $p$)

The "discrete" part of the name comes from the fact that the problem deals with discrete rather than continuous values. The security of many cryptographic systems relies on the difficulty of solving the DLP. In practice, the values of $g$, $y$, and $p$ are known, but $x$ is kept secret. The infeasibility of solving for $x$ in a reasonable amount of time is what makes the cryptographic system secure.

DLP is particularly important in public key cryptographic systems like [Diffie-Hellman](../cryptography/dh.md) key exchange and the [ElGamal](../cryptography/egl.md) encryption system. These systems allow secure communication over an insecure channel without the need to share a secret key in advance.

A variant of the DLP, known as the [Elliptic Curve Discrete Logarithm Problem (ECDLP)](../cryptography/ecdlp.md), is used in elliptic curve cryptography. ECDLP is similar to the traditional DLP but is defined over elliptic curves rather than the multiplicative group of integers modulo $p$.

The difficulty of the DLP increases significantly with the size of $p$$. For small values, it is relatively easy to solve, but for large values (hundreds of digits), no efficient general solution method is known. This asymmetry – easy to perform, hard to reverse – is a cornerstone of cryptographic systems based on the DLP, providing a way to create secure keys and encrypt data.
