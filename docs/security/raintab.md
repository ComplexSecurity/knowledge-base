Rainbow tables are a data structure used in cryptography, specifically for cracking encrypted passwords. They are a form of precomputed hash table, designed for reversing cryptographic hash functions, mainly to crack password hashes.

When passwords are stored securely, they are often hashed using a cryptographic hash function. The function converts the password into a fixed-size string of characters which is the hash. Hash functions are designed to be one-way making it computationally difficult to reverse it.

Rainbow tables are used to reverse these hash functions. They are essentially large databases that contain precomputed hashes of many possible plaintext passwords.

By comparing the hash from a password-protected system to the hashes in the rainbow table, one can identify the original password if a match is found.

Creating a rainbow table involves selecting a set of plaintexts (like all possible passwords up to a certain length), hashing them, and storing the result in a way that allows for efficient lookup. 

This process is time and resource-intensive but only needs to be done once. Once created, the table can be used repeatedly to crack different hashes.