Hexadecimal (often shortened to "hex") is a base-16 number system used in mathematics and computing. It uses sixteen distinct symbols, 0-9 to represent values zero to nine, and A-F (or a-f) to represent values ten to fifteen. Each hex digit represents four binary digits (bits), which makes it a convenient way to represent binary data in a more compact and human-readable form.

In the context of [[obfuscation]], hexadecimal encoding is used to disguise data, including code, to make it less readable and understandable to humans, thus adding a layer of complexity for anyone trying to analyze it.

Textual data, such as strings in a script, can be encoded in hexadecimal. For example, the [[ASCII]] string "hello" can be represented in hex as **68 65 6c 6c 6f.**

In programming, especially in web technologies like [[JavaScript]], hexadecimal encoding can be used to hide the true purpose or logic of the code. For instance, instead of using plain strings or numbers, a developer might use their hex equivalents.

Hexadecimal is used in character escaping where characters in strings are represented using hex values. This is commonly seen in [[URL encoding]], and the same principle can be applied to obfuscate code.

Since hex is more compact than binary, it’s often used to represent binary data in a more space-efficient manner. This can be part of a larger obfuscation strategy to make the binary data less recognizable.

Hexadecimal encoding is usually combined with other obfuscation methods like [[Javascript minification|minification]], renaming variables, string concatenation, and encoding with other bases (like base64) to increase the obfuscation level.