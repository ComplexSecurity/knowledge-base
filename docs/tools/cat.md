Hashcat is a powerful and widely-used password recovery tool that supports a wide array of hashing algorithms. It's designed for both [brute-force](../security/brute.md) and [dictionary-based attacks](../security/dict.md), allowing for the recovery of hashed passwords. 

Hashcat is notable for its speed and efficiency, particularly when leveraging the processing power of GPUs (Graphics Processing Units).

Hashcat supports a vast range of hashing algorithms, including popular ones like [MD5](../cryptography/md5.md), [SHA-1](../cryptography/sha1.md), [SHA-256](../cryptography/sha256.md), [NTLM](../security/ntlm.md), and many others. One of the most significant advantages of Hashcat is its ability to use the power of GPUs, which greatly increases the speed of password cracking compared to CPU-only cracking.

Hashcat supports various modes of operation, including brute-force attack, combinator attack, dictionary attack, [hybrid attack](../security/hybrid.md) (combining dictionary and brute-force methods), and more. Hashcat offers features like rule-based attack, which allows for complex password cracking strategies, and mask attack, for customizing brute-force attack patterns.

A basic example of using Hashcat for cracking a password might involve:

1. **Identifying the Hash Type**: Determine the type of hash algorithm used for the password (e.g., MD5, SHA-256).
2. **Setting Up Hashcat**: Configure Hashcat with the identified hash type and choose the attack mode (e.g., brute-force, dictionary).
3. **Running Hashcat**: Execute Hashcat against the hashed passwords. For a dictionary attack, you would also specify the path to your wordlist.

```bash
hashcat -m [hash type] [hash file] -a [attack mode] [wordlist]
```

