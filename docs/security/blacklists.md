In the context of web application penetration testing (pentesting), a "blacklist" refers to a security mechanism that blocks or restricts certain elements, inputs, or actions based on a predefined list of disallowed items. This concept is often used to prevent potentially harmful operations or data from entering or interacting with a system.

Blacklists are commonly used in input validation processes. Web applications check user inputs against a list of forbidden characters, strings, or patterns to prevent malicious data, such as [[SQL injection]] or [[Cross-Site Scripting]] (XSS) payloads, from being processed.

Blacklists can be implemented as filters in various parts of a web application, including form inputs, URLs, and [[file uploads]], to block known malicious content.

Items often found on blacklists include certain special characters (like `<`, `>`, `'`, `"`), SQL keywords (like `SELECT`, `DROP`), and scripting elements (like `<script>`, `alert()`).

The effectiveness of blacklisting is limited because it's often impossible to predict and enumerate all possible malicious inputs or actions. Attackers can bypass blacklists using encoding, obfuscation, or other evasion techniques. Maintaining an exhaustive blacklist can be challenging and impractical, particularly as new vulnerabilities and attack vectors emerge.

Blacklisting is often contrasted with [[Whitelists|whitelisting]], which allows only known safe inputs or actions. Whitelisting is generally considered more secure but can be more restrictive and harder to implement effectively.

During pentesting, testers often attempt to bypass blacklists to demonstrate how an attacker might exploit insufficient or improperly implemented input validation. Blacklisting is a part of a defense-in-depth strategy. It should be used in conjunction with other security measures like whitelisting, secure coding practices, and regular security audits.

