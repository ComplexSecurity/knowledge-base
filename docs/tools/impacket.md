Impacket is an open-source collection of [[Python]] classes for working with network protocols. It is widely used in the field of network security and penetration testing. Impacket is designed to provide low-level programmatic access to the packets and, for some protocols, to the higher-level functionalities like authentication, connection, etc.

Impacket includes support for a variety of network protocols, including [[Internet Protocol (IP)|IP]], [[Transmission Control Protocol|TCP]], [[User Datagram Protocol|UDP]], [[ICMP]], [[Server Message Block|SMB]], [[Microsoft Remote Procedure Call|MSRPC]], [[NetBIOS Message Block (NMB)|NMB]], and others. This makes it a versatile tool for network protocol analysis and manipulation. It allows for the creation and manipulation of network packets. This is useful for testing the security and resilience of network applications and services.

For some protocols like SMB, Impacket provides high-level functionalities such as performing authentication and establishing connections. Impacket can be used to write scripts that automate common network tasks, such as gathering information, exploiting vulnerabilities, or establishing connections with network services.

Security professionals and penetration testers use Impacket to exploit known vulnerabilities in network protocols or services. For example, it can be used to exploit weaknesses in SMB/[[CIFS]] protocols on Windows machines. Impacket scripts can gather information about networked systems, test protocols, and analyze network security.

It can be used to perform [[Pass-the-Hash Attacks]], [[Relay Attacks]], or extract [[NTLM]] credentials from network traffic.

Here’s an example of how Impacket might be used in a script (note that this is a conceptual example for illustrative purposes):

```python
from impacket.smbconnection import SMBConnection

# Establish a connection to the SMB server
smb = SMBConnection("TARGET_MACHINE", "TARGET_MACHINE_IP")
smb.login("username", "password")

# List shares available on the target machine
shares = smb.listShares()
for share in shares:
    print(share['shi1_netname'])

# Other operations with the SMB connection
```

!!! info
    Impacket is used to connect to an SMB server, authenticate, and list the available shares.

Impacket provides a suite of powerful tools that leverage its Python classes for various network protocols. These tools are particularly useful in the context of network security and penetration testing. Some of the common tools included in the Impacket collection are:

1. [[smbserver]]: A simple SMB/CIFS server that can be used for file sharing, uploading, and downloading. It's useful in scenarios where you need a quick SMB server setup for testing or exploitation purposes.
2. [[psexec]]: A tool that provides functionality similar to [[Microsoft PsExec|Microsoft's PsExec]] utility. It allows execution of processes remotely by creating a service on the remote system.
3. [[mssqlclient]]: A minimalistic [[Microsoft SQL Server|MSSQL]] client that allows connecting to SQL servers, executing queries, and performing database operations. It supports both Windows and SQL Server authentication.
4. [[ntlmrelayx]]: A tool for performing NTLM relay attacks. It can capture NTLM authentication requests and relay them to other services, potentially allowing unauthorized access.
5. [[secretsdump]]: Used for extracting various types of credentials from Windows systems, such as NTLM password hashes, [[Kerberos tickets]], and [[LSA (Local Security Authority)|LSA]] secrets.
6. [[GetADUsers]]: A tool for gathering information about users in a Microsoft [[Active Directory]] environment. It can be used to enumerate users, their last login times, and password expiration dates.
7. [[GetNPUsers]]: This tool attempts to list and get [[Kerberos Ticket Granting Ticket (TGT)|TGTs]] for those users that have the property 'Do not require Kerberos preauthentication' set in a [[Domain Controller]]. Useful for [[Kerberoasting]] attacks.
8. [[GetUserSPNs]]: Used in Kerberoasting attacks, this tool requests [[Service Principal Names (SPN)|Service Principal Names]] (SPN) to get TGS tickets that can be cracked offline.
9. [[lookupsid]]: Allows you to perform [[Windows SID (Security Identifier)|SID]] enumeration on Windows systems to gather information about existing user accounts.
10. [[smbrelayx]]: Similar to [[ntlmrelayx]], it's used for SMB relay attacks, where SMB sessions are relayed to other targets.
11. [[wmiexec]]: A tool that provides a semi-interactive shell, allowing the execution of commands via [[Windows Management Instrumentation (WMI)|WMI]].
12. [[smbclient]]: A simple SMB client that allows for file and directory browsing, file uploading, downloading, and deletion on SMB shares.