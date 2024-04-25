A reverse shell in the context of penetration testing (pentesting) is a technique used to establish a command line session with a target system, where the target system initiates the connection back to the attacker’s machine. This is often used by pentesters and cyber attackers to bypass [[firewall]] protections that may block incoming connections.

In a typical shell or command line access, you connect to another system (e.g., using [[Secure Shell|SSH]] or [[Telnet]]) to execute commands. This is a forward connection. A reverse shell reverses this process. The target system connects back to the attacker’s system, which is listening for incoming connections.

Firewalls often block incoming connections to certain ports but allow outgoing connections from internal network. A reverse shell exploits this by initiating the connection from the target machine (which is usually allowed through the firewall).

Similarly, it's effective in scenarios where the target is behind a [[Network Address Translation (NAT)|NAT]] (Network Address Translation), making direct connections difficult. 

Once a vulnerability is exploited (like a [[Buffer Overflows|buffer overflow]], [[SQL injection]], etc.), the pentester can use that foothold to execute a payload that opens a reverse shell. The pentester’s machine listens on a specified port. When the reverse shell is executed on the target system, it connects back to the pentester’s listening service, giving command line access to the target system.

Reverse shells can be scripted in various programming languages like [[Python]], [[PHP]], [[Perl]], or [[bash]], depending on what resources are available on the target system. Tools like [[Netcat]], nc, or advanced frameworks like [[Metasploit Framework|Metasploit]] can be used to create and handle reverse shells.