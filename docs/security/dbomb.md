A decompression bomb, also known as a "Zip bomb" or "compression bomb," is a maliciously crafted file designed to crash or render useless the program or system reading it. It's a type of attack against a system's file decompression functionality.

A decompression bomb is typically a small compressed file that, when decompressed, expands to an enormous size far beyond the system's capacity to handle. For example, a few kilobytes of compressed data could expand into gigabytes or terabytes.

The primary goal of a decompression bomb is to consume system resources, thereby causing performance issues, exhausting storage space, or crashing the system. This can be part of a [Denial of Service (DoS) Attacks|denial-of-service (DoS) attack]().

Although often associated with ZIP files, decompression bombs can be created in any file format that supports compression, such as gzip, rar, or tar. These files are created using recursive or repeating patterns that compress well but expand to a disproportionately large size when decompressed.

Decompression bombs can impact software that automatically decompresses files, such as email servers, web servers, antivirus programs, or file decompression utilities.
