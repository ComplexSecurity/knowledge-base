Incognito is a module within the [[Metasploit Framework]], an open-source penetration testing tool. It is specifically designed for [[privilege escalation]] and impersonation in Windows environments. Incognito focuses on exploiting Windows access token vulnerabilities to escalate privileges and impersonate logged-in users, particularly in post-exploitation phases of a penetration test.

Incognito can enumerate and impersonate user tokens available on a compromised Windows system. Windows access tokens are objects that describe the security context of a process or thread and contain information about the user account associated with the process. By impersonating tokens with higher privileges, Incognito allows penetration testers or attackers to escalate their privileges on the compromised system.

With elevated privileges, it becomes possible to access resources that were previously restricted, such as files, directories, or services requiring higher-level permissions.

After gaining initial access to a system, Incognito is used to list available tokens. These tokens represent the security contexts of users currently logged into the system or services running under certain user accounts. The penetration tester or attacker can then select and impersonate a token belonging to a higher-privileged user or service account. Once impersonating a higher-privileged token, the attacker or tester can execute actions that require elevated privileges, such as accessing sensitive data, installing additional tools, or moving laterally across the network.

Imagine a scenario where a penetration tester has gained access to a standard user account on a Windows server. The server also has an administrator account currently logged in:

1. **Enumeration**: The tester uses Incognito to list all available tokens on the server.
2. **Impersonation**: Among the listed tokens, the tester finds a token associated with the administrator account.
3. **Elevated Access**: By impersonating the administrator's token, the tester gains full administrative privileges on the server, allowing them to conduct further exploration or demonstrate the impact of a full system compromise.

