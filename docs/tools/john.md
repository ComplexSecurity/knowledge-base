John the Ripper is a widely used open-source [password cracking](../security/crack.md) tool. It's designed to detect weak passwords by trying to crack hashed passwords recovered from a system's shadow file or obtained from other sources. John the Ripper uses a variety of techniques, including [brute force](../security/brute.md) and [dictionary attacks](../security/dict.md), to guess passwords.

It typically operates on password hashes. When you enter a password into a system, that password is usually not stored directly; instead, it's processed through a cryptographic hash function, and the resulting hash is stored. John the Ripper first tries a dictionary attack, where it runs through a list of common passwords (from a wordlist) and their precomputed hash values.

If the dictionary attack fails, it employs brute-force attacks, generating every possible password combination until it finds a match. It also applies various mangling rules to dictionary words (like adding numbers, capitalizing letters, or reversing characters) to guess more complex passwords that might be derived from simple words.

Suppose you have a file containing password hashes named `hashes.txt`. To attempt cracking these passwords with John the Ripper, you would use the following syntax in the command line:

```bash
john hashes.txt
```

This command tells John the Ripper to start cracking the hashes in `hashes.txt` using its default settings and wordlists. You can also specify different modes and options. For example, to use a specific wordlist, you can use the `--wordlist` option followed by the path to your wordlist file.

```bash
john --wordlist=/path/to/wordlist.txt hashes.txt
```

To enable rules (which apply various transformations to wordlist entries), you can use the `--rules` option.

```bash
john --wordlist=/path/to/wordlist.txt --rules hashes.txt
```

If you want to use brute-force mode, you can specify it with `--incremental`.

```bash
john --incremental hashes.txt
```

To display the passwords that have been successfully cracked, use the `--show` option.

```bash
john --show hashes.txt
```

If you know the type of hash algorithm used (e.g., MD5, SHA-256), you can specify it with the `--format` option:

```bash
john --format=md5crypt hashes.txt
```

!!! info
    This command tells John the Ripper to specifically use the MD5 hash algorithm when attempting to crack the hashes in `hashes.txt`.