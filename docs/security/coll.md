Collision attacks are a type of cryptographic attack on hash functions, a critical component in various security applications like digital signatures and data integrity verification. In a collision attack, the goal is to find two different inputs that produce the same hash output, thereby causing a "collision" in the hash function.

There are two types:

1. **Birthday Attack**: This is based on the birthday paradox in probability theory. The attack involves finding two different inputs that hash to the same output. It's called a "birthday attack" because it exploits the mathematical principle that in a group of people, it's surprisingly likely that two will share the same birthday. In hash functions, it means that it's more feasible than intuitively expected to find two different inputs with the same hash.
2. **Specific-Input Collision**: In this case, an attacker tries to find a collision for a specific given input. This is typically harder than a general collision attack.

Hash functions are used to ensure data integrity. If an attacker can produce a collision, they can replace legitimate data with fraudulent data having the same hash value, potentially bypassing systems that rely on hashes for data integrity checks.

Collision attacks can undermine digital signature schemes. If an attacker can generate a collision, they might be able to forge a digital signature, making it appear as though a trusted source signed a malicious document or file.

[[MD5]], an older hash function, is known to be vulnerable to collision attacks. It's possible to create two different documents that hash to the same MD5 hash, allowing for potential security breaches. Similar vulnerabilities have been discovered in [[SHA-1]], leading to its deprecation in favour of more secure hash functions like [[SHA-256]].

The best defense against collision attacks is using modern, secure hash functions like [[SHA-256]] or [[SHA-3]], which are designed to be resistant to such attacks. As vulnerabilities are discovered, it's important for organizations to update their cryptographic practices and move to more secure algorithms.
