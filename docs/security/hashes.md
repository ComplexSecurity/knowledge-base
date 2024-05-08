Password hashes are cryptographic representations of passwords that are stored in a secure manner to protect user credentials. Instead of storing passwords in plain text, which is highly insecure, systems store password hashes. A password hash is the result of applying a cryptographic hash function to the user's password.

When a user creates or changes their password, the system applies a cryptographic hash function to the password. This function generates a fixed-length string of characters (the hash) from the password. The same password will always produce the same hash.

Hash functions produce output of a fixed length, regardless of the input length. For example, a common hash function, [SHA-256](), produces a 256-bit (32-byte) hash value. A strong cryptographic hash function is designed to be a one-way function. It should be computationally infeasible to reverse the process and obtain the original password from the hash. This property ensures that even if the hash is compromised, the attacker cannot easily determine the password.

To further enhance security, a unique random value called a "[Salt]()" is often generated for each user. The salt is combined with the password before hashing. Salting prevents attackers from using precomputed tables (rainbow tables) to look up common passwords' hashes.

The resulting password hash and the salt (if used) are stored in the system's database. The plain text password is not stored. When a user attempts to log in, the system hashes the entered password with the stored salt (if applicable) and compares it to the stored hash.

During login, the system retrieves the stored hash and salt (if used), applies the hash function to the entered password with the stored salt, and compares the result to the stored hash. If they match, the entered password is correct.

Security best practices include using strong, well-established hash functions (e.g., SHA-256), generating unique salts for each user, and periodically rehashing passwords to protect against advanced attacks.
