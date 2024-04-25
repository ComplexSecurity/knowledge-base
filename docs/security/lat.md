Lateral movement in penetration testing refers to the techniques used by penetration testers (or attackers in a malicious scenario) to move through a network after gaining initial access. The goal is to expand access to more systems and potentially increase privileges, to reach high-value targets like data servers, [[Domain Controller|domain controllers]], or administrative systems.

Some techniques for lateral movement:

1. Exploiting Weak Credentials: Using default or weak credentials to access other systems on the network.
2. [[Pass-the-Hash Attacks|Pass-the-Hash]]/[[Pass-the-Ticket Attacks|Pass-the-Ticket]]: Using captured hash values or [[Kerberos tickets]] from one machine to authenticate to others.
3. **Remote Services Exploitation**: Utilizing services like [[Remote Desktop Protocol]] (RDP), [[Secure Shell]] (SSH), or [[WinRM|Windows Remote Management (WinRM)]] to access and control other systems.
4. **Session Hijacking**: Taking over existing user sessions on other machines.
5. **Privilege Escalation**: Gaining higher-level privileges to access more secured parts of the network.

Some tools also include:

1. [[Mimikatz]]: Used for extracting credentials, such as plaintext passwords, [[NTLM]] hashes, and [[Kerberos tickets]], from memory.
2. [[Microsoft PsExec|PsExec]]: A part of [[Sysinternals Suite]], it's used to execute processes remotely, leveraging administrative credentials.
3. [[Empire|PowerShell Empire]]: A post-exploitation framework that allows extended control over compromised machines and can be used for moving laterally.
4. [[Metasploit Framework]]: Contains various modules to exploit vulnerabilities, execute payloads, and move laterally in a network.
5. [[BloodHound]]: Uses graph theory to reveal hidden and often unintended relationships within [[Active Directory]] environments, helpful in planning lateral movement paths.

Some examples include:

- Using PsExec with Stolen Credentials: A penetration tester, after obtaining administrative credentials from one workstation, uses PsExec to remotely execute commands on another workstation or server.
- Pass-the-Hash Attack: The tester uses a captured NTLM hash from one machine to authenticate to another machine on the network.
- Exploiting Vulnerabilities: If a vulnerability like [[SMB Relay Attacks|SMB Relay]] or [[EternalBlue]] is found on another machine in the network, it could be exploited to gain unauthorized access.