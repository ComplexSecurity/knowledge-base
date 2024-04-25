Token Impersonation is a technique in computer security, particularly in Windows environments, where an attacker or a process gains unauthorized access by using an authentication token of another user or process. In Windows, authentication tokens represent the security context of a user or process, including their identity and privileges.

When a user logs in or a process runs, Windows creates an access token that contains security information about that session. If an attacker gains access to a system, they can potentially access the tokens of other users or processes. The attacker can then use a technique called impersonation, where they adopt the token of another user or process. This allows them to perform actions on the system with the same rights and privileges as that user or process.

Often, token impersonation is used for [[privilege escalation]]. For example, if an attacker can impersonate a token of a user with administrative privileges, they can gain control over the entire system. After gaining initial access to a system, attackers or penetration testers use token impersonation to elevate their privileges and deepen their access.

Tools like [[Incognito]] (part of [[Metasploit Framework|Metasploit]]), [[Mimikatz]], and others can be used to find and impersonate tokens. Impersonating a token can also facilitate lateral movement within a network, allowing attackers to access other systems using the credentials of the impersonated token.

