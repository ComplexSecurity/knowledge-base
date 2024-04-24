Base64 is a binary-to-text encoding scheme that is used to represent binary data in an [[ASCII]] string format. It's commonly used in various applications where data needs to be encoded to safely be transmitted over media that are designed to handle text.

Base64 encoding takes binary data and divides it into groups of 6 bits. Since 6 bits can represent 64 different values (2^6 = 64), each 6-bit group is then mapped to a specific character from a set of 64 characters. The Base64 index table includes uppercase and lowercase letters (A-Z, a-z), digits (0-9), and a couple of special characters (+ and /).

If the total number of bits in the binary data is not a multiple of 6, the last group will be padded with zeros to make it a full 6-bit group. Correspondingly, the Base64 output is padded with '=' characters to indicate that padding occurred.

The standard Base64 character set includes:

- Uppercase letters
- Lowercase letters
- Digits
- Plus sign
- Slash
- Equals sign


