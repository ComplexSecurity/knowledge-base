A web shell is a type of malicious script or program that enables remote administration of a web server. Once uploaded and executed on a web server, a web shell allows an attacker to perform various tasks on the server, typically through a browser interface. It acts as a backdoor, granting the attacker a level of control over the server and its contents.

The primary function of a web shell is to provide the attacker with remote management capabilities of the web server, allowing them to execute server commands from a remote location.

Web shells are often uploaded to a server as part of another exploit, such as a [[SQL injection]] or a file upload vulnerability in a web application. They can be written in any scripting language supported by the server, like [[PHP]], [[ASP.NET|ASP]], [[JSP]], or [[Perl]].

Once uploaded, the web shell script presents a user interface (often web-based) that allows the attacker to execute server commands. These commands might include creating, deleting, downloading, or modifying files; accessing databases; launching additional attacks; or even using the server to propagate the attack to other systems.

Attackers can steal or manipulate data on the server or connected systems. They can use the server to host illicit content, such as [[phishing]] pages or illegal files. Compromised servers can be used as a platform for launching attacks against other targets, including [[Denial of Service (DoS) Attacks|DDoS attacks]].

Web shells can be difficult to detect because they often mimic legitimate files and have a small footprint. They might be obfuscated to evade detection by security tools.
