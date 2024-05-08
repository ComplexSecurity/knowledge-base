A bind shell is a type of shell used in cybersecurity contexts, particularly in the exploitation of vulnerable systems. It refers to a technique where a shell (command interpreter) is bound to a specific [port]() on the target machine, allowing an attacker to remotely access it.

In a bind shell scenario, an attacker exploits a vulnerability in a target system to execute arbitrary code. This code sets up a command shell (like bash, cmd.exe) that listens on a specified network port.

Once the shell is bound to a port, the attacker can connect to this port over the network. This connection provides access to the command shell of the target system, allowing the attacker to execute commands as if they were locally logged into the system.

Unlike a [Reverse Shell](), where the target system initiates a connection to the attacker’s machine, a bind shell opens a listening port on the target system, which the attacker then connects to. Bind shells are often used in penetration testing and exploitation scenarios to demonstrate the impact of a vulnerability that allows remote code execution.

Bind shells are considered a security threat, as they allow unauthorized access to a system. They can bypass [Firewall|firewalls]() and other security measures if outbound traffic is less restricted than inbound traffic.

Bind shells can be scripted in various languages (like [Python](), [Perl](), [PHP]()) or set up using tools like [Netcat]().
