A second-order [Local File Inclusion]() (LFI) attack is a more complex form of the standard LFI attack. In a typical LFI attack, an attacker manipulates input to include files that are already on the server (like `/etc/passwd`) into the output of a web application. 

However, in a second-order LFI attack, the malicious file inclusion is performed in two steps, making it more insidious and harder to detect.

The attacker interacts with the web application in a way that allows them to upload or modify a file on the server. This could be through features like profile picture upload, file sharing, or document editing. Instead of a legitimate file, the attacker uploads or inserts malicious content (e.g., a [PHP]() script) into a file. This file is saved on the server, but it's not immediately executed.

Later, the attacker manipulates the application to include the file they uploaded or modified. This is typically done by exploiting vulnerabilities in the application that allow for file inclusion, such as poorly sanitized input parameters. When the application includes the uploaded/modified file in its execution context (for example, through a dynamic file include mechanism), the malicious code gets executed.

Some example scenarios include:

- **File Upload**: An application allows users to upload a custom profile template, which is stored as a file on the server.
- **Malicious Upload**: An attacker uploads a file named `custom_template.php` containing a PHP script that can execute arbitrary commands on the server.
- **Delayed Execution**: Initially, this file just sits on the server without causing harm.
- **Manipulating File Inclusion**: Later, the attacker manipulates a different feature of the application, such as a dynamic template rendering function, to include `custom_template.php`.
- **Code Execution**: When an unsuspecting user or admin accesses the feature that includes the attacker’s template, the malicious PHP script is executed, potentially compromising the server.