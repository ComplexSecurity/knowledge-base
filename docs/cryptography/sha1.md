SHA-1 (Secure Hash Algorithm 1) is a cryptographic hash function designed by the National Security Agency (NSA) and published by the National Institute of Standards and Technology (NIST) in 1995. It produces a 160-bit (20-byte) hash value, typically rendered as a 40-digit hexadecimal number. SHA-1 is part of the SHA family of algorithms.

Regardless of the input size, SHA-1 generates a fixed-size 160-bit hash. The hash is designed to be unique; different inputs should yield different hashes (though this has been compromised over time). The same input always results in the same hash output.

It was initially favored for its speed and efficiency in generating hashes. It's computationally infeasible to reverse the hash function to retrieve the original input data.

It is used to ensure data integrity by generating a hash of the data and then verifying the hash at the receiving end. Utilized in digital signature algorithms to ensure the authenticity of digital documents.

It is also employed in [[SSL-TLS|SSL/TLS]] [[SSL certificates|certificates]] for securing websites (though this use has been phased out). It was also used to verify the integrity of software packages by comparing the hash of the downloaded file with a published hash.

Over time, vulnerabilities in SHA-1 have been discovered, including the potential for collision attacks (where two different inputs produce the same hash). These vulnerabilities compromise its security effectiveness. Due to these vulnerabilities, SHA-1 has been increasingly phased out in favor of more secure algorithms like [[SHA-256]] and [[SHA-3]].

An example of a SHA-1 hash of the string "Hello, world!" might look like this:

```bash
7f83b1657ff1fc53b92dc18148a1d65dfc2d4b1f
```

