CrackMapExec (CME) is a versatile tool for penetration testers and cybersecurity professionals, designed to facilitate the assessment and exploitation of large [[Active Directory]] networks. Developed in [[Python]], CrackMapExec automates the exploitation of common vulnerabilities in Windows environments, streamlining the process of post-exploitation and network reconnaissance.

CME can be used to gather information about Windows machines on a network, including OS details, hostname, domain information, and [[Server Message Block|SMB]] shares. It can test the validity of credentials across a network, helping identify machines where a given set of credentials is valid.

CME supports [[pass-the-hash attacks]] and [[Token Impersonation|token impersonation]], allowing penetration testers to leverage compromised credentials or tokens to access other network resources. It can execute commands or [[Windows PowerShell]] scripts remotely on Windows machines. CrackMapExec is modular, allowing for the easy integration of additional functionalities through its module system.

Some examples of its usage include enumerating SMB shares:

```bash
crackmapexec smb <TARGET_IP> --shares
```

Validating credentials:

```bash
crackmapexec smb <TARGET_IP_RANGE> -u <USERNAME> -p <PASSWORD>
```

Executing commands:

```bash
crackmapexec smb <TARGET_IP> -u <USERNAME> -p <PASSWORD> -x 'whoami'
```

Pass-The-Hash attack:

```bash
crackmapexec smb <TARGET_IP_RANGE> -u <USERNAME> -H <NTLM_HASH>
```
