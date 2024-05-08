Code deobfuscation refers to the process of transforming obfuscated code, which is intentionally made complex and difficult to understand, back into its more readable and comprehensible form.

This process is commonly used in software analysis, especially when dealing with code that has been obfuscated for various reasons.

Code is often obfuscated to protect intellectual property, hinder reverse engineering or conceal malicious content. Obfuscation techniques can include altering variable names, restructuring code, or using complex algorithms to mask the code's true function.

Deobfuscation involves various techniques like [Static Analysis|static analysis](), [Dynamic Analysis|dynamic analysis](), and the use of specialised tools. Static analysis involves examining the code without executing it, while dynamic analysis involves running the code and observing its behaviour.

Deobfuscation can be challenging as [Obfuscation (KB)|obfuscation]() techniques are designed to make reverse engineering more difficult. It is commonly used in cybersecurity for analysing malware, in software development for understanding legacy code or third-party components.

[JavaScript](), being a widely-used language for web development, is often targeted for obfuscation to protect client-side code. Some common obfuscation techniques for JavaScript include:

- Minification - removing whitespace, newlines, and comments and shortening variable names.
- String Encoding - encoding strings in a non-standard format.
- Code Transformation - changing the code structure without altering its functionality.
- Logic Bombs - inserting conditional statements that change the code behaviour under certain conditions.
