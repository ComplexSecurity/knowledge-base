WinRM (Windows Remote Management) is Microsoft's implementation of WS-Management Protocol (Web Services-Management), a standard protocol for remote management of computers. It allows administrators to remotely run management scripts and access data on Windows-based systems across a network.

WinRM enables administrators to interact with Windows machines remotely, executing [PowerShell](../tools/ps.md) scripts and commands, and managing system settings. It uses the WS-Management protocol, which is based on standard web services, allowing for interoperability across different systems and platforms. WinRM can be configured to use [HTTPS](../web/https.md) for encrypted communications, enhancing security for remote management activities.

WinRM is often used in conjunction with Windows PowerShell for advanced remote administration and automation tasks. In the context of hacking or penetration testing, WinRM can be a vector for both attack and defense:

1. [Lateral Movement](../security/lat.md): Once an attacker gains access to a network, they can use WinRM to move laterally across the network, executing commands on other Windows machines.
2. [Remote Code Execution](../security/rce.md): If WinRM is enabled and accessible, and if the attacker has valid credentials, it can be used to execute arbitrary code remotely.
3. [Persistence](../security/persist.md): Attackers might use WinRM to establish persistence on a network, enabling them to maintain access even after initial entry points are closed.
