**Remote code execution (RCE)** refers to a class of cyberattacks in which attackers remotely execute commands to place malware or other malicious code on your computer or network. In an RCE attack, there is no need for user input from you. A remote code execution vulnerability can compromise a user’s sensitive data without the hackers needing to gain physical access to your network.

Remote code execution attacks generally occur via vulnerabilities in web applications and network infrastructure.

Remote code execution vulnerabilities are flaws in software that allow an attacker to run malicious code on a target system. Several types of vulnerabilities can be used for RCE, including the following examples:

- **Injection vulnerabilities:** An injection vulnerability — such as [[SQL injection]] or [[Command Injection]] — is enabled by poor input sanitization. If a user provides a carefully-crafted, malicious input, some of their provided data will be interpreted as commands to be run. This allows the attacker to force the vulnerable system to execute attacker-provided code.
- **Insecure deserialization:** Serialization simplifies the transmission of sets of data by packing it into a single string of bits to be unpacked by the recipient system. However, if the structure of serialized data is not well defined, an attacker may be able to craft an input that is misinterpreted when it is unpacked. Depending on how the data is stored and processed, this misinterpretation may allow the attacker to achieve code execution.
- **Out-of-bounds write:** A buffer is a fixed-size piece of memory that is allocated to store data. Insecure data reads or writes could allow an attacker to place data where it would be interpreted as code or as important control flow information for the application.
- **File management:** Some applications allow users to upload files to a server. The access that this provides may allow an attacker to upload a file containing malicious code and trick the application into executing it.

Malware is attacker-provided code that is designed to be executed on a target system. An RCE vulnerability simply allows an attacker to deploy malware in different ways.

As a result, RCE vulnerabilities can be used to achieve many of the same goals as traditional malware. RCE can be used to deploy malware on a vulnerable system, perform a denial-of-service (DoS) attack, or access sensitive information stored on a system.