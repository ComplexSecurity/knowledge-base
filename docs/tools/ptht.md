The "PTH-Toolkit" is a set of tools designed to facilitate [[Pass-the-Hash Attacks|pass-the-hash (PtH) attacks]] in penetration testing and security assessment scenarios. Pass-the-hash is a technique where an attacker uses a hashed user credential (rather than the plaintext password) to authenticate to remote servers or services. The PTH-Toolkit leverages this approach to test and exploit systems that are vulnerable to this type of attack.

The toolkit allows for the use of [[NTLM]] or [[LanMan]] hashes to authenticate against various Windows services and protocols, such as [[Server Message Block|SMB]], [[WinRM|WinRM]], and [[Remote Desktop Protocol|RDP]]. The toolkit typically includes tools for various protocols, enabling attackers to test multiple attack vectors within a network. It can be used in conjunction with other tools to extract hashes from a system (like [[Mimikatz]]) and then use those hashes for further exploitation.

While the specific contents of the PTH-Toolkit can vary, it generally includes tools like:

- **pth-winexe**: For executing commands remotely using a hash.
- **pth-wmic**: For performing [[Windows Management Instrumentation (WMI)|WMI]] queries with a hash.
- **pth-smbclient**: A version of [[smbclient]] that accepts NTLM hashes.
- **pth-mssqlclient**: For authenticating to SQL Servers using a hash.

An example of using a tool from the PTH-Toolkit might be:

```bash
pth-winexe -U DOMAIN/user%aad3b435b51404eeaad3b435b51404ee:ed2b1f468c5f915f9cbe9e2fa1c6d345 //<TARGET_IP> cmd.exe
```

- `-U DOMAIN/user%hash` specifies the domain, username, and NTLM hash for authentication.
- `<TARGET_IP>` is the IP address of the target machine.
- `cmd.exe` is the command to be executed on the remote system.

