Null byte injection is a type of attack that exploits a vulnerability in a computer program where a null byte (`\0`) is used to manipulate the control flow or data interpretation. The null byte, often represented in programming languages like [C]() and [C++]() as `'\0'`, is used to signify the end of a string.

In languages like C and C++, strings are terminated with a null byte. This is how the program knows where the string ends. An attacker injects a null byte into a data stream or input field that the program will process.

When the program encounters the null byte, it interprets it as the end of the string, effectively truncating or altering the data that follows the null byte. This behavior can be exploited in various ways, depending on the context and the program's logic.

An attacker might add a null byte to manipulate file paths. For example, the input `malicious.php\0.png` could be used to upload a [PHP]() file while the system only checks for a `.png` extension. The server might validate the extension as `.png`, but when accessing the file, the server-side language (like PHP) stops reading the path at `\0`, executing `malicious.php`.

Null byte injection can be used in conjunction with [Buffer Overflows|buffer overflow]() attacks to manipulate the execution flow of an application.

If a program sanitizes inputs by looking for dangerous characters or patterns but stops at a null byte, an attacker could inject code followed by a null byte to bypass the sanitization process.

