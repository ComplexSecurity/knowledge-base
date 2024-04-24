icon:material/apple

# Sha2

Set of cryptographic hash functions designed to provide strong data integrity checks and security.

## Installation

```bash
brew install sha2
```

## Usage

```bash
sha2 [options] [<file>]
```

## Flags

```bash
-256    Generate SHA-256 hash
-384    Generate SHA-284 hash
-512    Generate SHA-512 hash
-ALL    Generate all three hashes
-q      Quiet mode - only output hexadecimal hashes, one per line
```

## Examples

```bash
sha2 -256 kali-linux-2022.3-installer-netinst-amd64.iso
SHA-256 (kali-linux-2022.3-installer-netinst-amd64.iso) = 82f702acf37771ac27355c5f9170bf365a73f0cc9e571fb422f7aa58ca218d48
```

## References

- [Formulae.brew.sh - sha2](https://formulae.brew.sh/formula/sha2#default)
- [Aarongifford - sha](https://aarongifford.com/computers/sha.html)
