A URL is composed from a limited set of characters belonging to the US-ASCII character set. These characters include digits (0-9), letters(A-Z, a-z), and a few special characters ("-", ".", "\_", "~").

ASCII control characters (e.g. backspace, vertical tab, horizontal tab, line feed etc), unsafe characters like space, \, <, >, {, } etc, and any character outside the ASCII charset is not allowed to be placed directly within URLs.

Moreover, there are some characters that have special meaning within URLs. These characters are called **reserved** characters. Some examples of reserved characters are ?, /, #, : etc. Any data transmitted as part of the URL, whether in query string or path segment, must not contain these characters.

To transmit these characters, they must be encoded.

URL Encoding converts reserved, unsafe, and non-ASCII characters in URLs to a format that is universally accepted and understood by all web browsers and servers. It first converts the character to one or more bytes. Then each byte is represented by two hexadecimal digits preceded by a percent sign (%) - (e.g. %xy). The percent sign is used as an escape character.

URL encoding is also called **percent encoding** since it uses percent sign (%) as an escape character.

One of the most frequent URL Encoded character you’re likely to encounter is **space**. The ASCII value of space character in decimal is 32, which when converted to hex comes out to be 20. Now we just precede the hexadecimal representation with a percent sign (%), which gives us the URL encoded value - %20.
