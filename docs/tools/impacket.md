Impacket is an open-source collection of [Python](../programming/python.md) classes for working with network protocols. It is widely used in the field of network security and penetration testing. Impacket is designed to provide low-level programmatic access to the packets and, for some protocols, to the higher-level functionalities like authentication, connection, etc.

Impacket includes support for a variety of network protocols, including [IP](../protocols/ip.md), [TCP](../networking/tcp.md), [UDP](../networking/udp.md), [ICMP](../networking/icmp.md), [SMB](../protocols/smb.md), [MSRPC](../misc/mrpc.md), [NMB](../protocols/nmb.md), and others. This makes it a versatile tool for network protocol analysis and manipulation. It allows for the creation and manipulation of network packets. This is useful for testing the security and resilience of network applications and services.

For some protocols like SMB, Impacket provides high-level functionalities such as performing authentication and establishing connections. Impacket can be used to write scripts that automate common network tasks, such as gathering information, exploiting vulnerabilities, or establishing connections with network services.

Security professionals and penetration testers use Impacket to exploit known vulnerabilities in network protocols or services. For example, it can be used to exploit weaknesses in SMB/[CIFS](../protocols/cifs.md) protocols on Windows machines. Impacket scripts can gather information about networked systems, test protocols, and analyze network security.

It can be used to perform [Pass-the-Hash Attacks](../activedirectory/pth.md), [Relay Attacks](../activedirectory/relayatt.md), or extract [NTLM](../security/ntlm.md) credentials from network traffic.

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

1. [smbserver](../tools/smbserver.md): A simple SMB/CIFS server that can be used for file sharing, uploading, and downloading. It's useful in scenarios where you need a quick SMB server setup for testing or exploitation purposes.
2. [psexec](../tools/psexec.md): A tool that provides functionality similar to [Microsoft's PsExec](../tools/mpsexec.md) utility. It allows execution of processes remotely by creating a service on the remote system.
3. [mssqlclient](../tools/mssqlc.md): A minimalistic [MSSQL](../databases/sqls.md) client that allows connecting to SQL servers, executing queries, and performing database operations. It supports both Windows and SQL Server authentication.
4. [ntlmrelayx](../tools/ntlmrelayx.md): A tool for performing NTLM relay attacks. It can capture NTLM authentication requests and relay them to other services, potentially allowing unauthorized access.
5. [secretsdump](../tools/secretsdump.md): Used for extracting various types of credentials from Windows systems, such as NTLM password hashes, [Kerberos tickets](../activedirectory/tickets.md), and [LSA](../misc/lsa.md) secrets.
6. [GetADUsers](../tools/getadusers.md): A tool for gathering information about users in a Microsoft [Active Directory](../activedirectory/activedirectory.md) environment. It can be used to enumerate users, their last login times, and password expiration dates.
7. [GetNPUsers](../tools/getnpusers.md): This tool attempts to list and get [TGTs]() for those users that have the property 'Do not require Kerberos preauthentication' set in a [Domain Controller](../activedirectory/dc.md). Useful for [Kerberoasting](../activedirectory/roasting.md) attacks.
8. [GetUserSPNs](../tools/getuspn.md): Used in Kerberoasting attacks, this tool requests [Service Principal Names](../security/spns.md) (SPN) to get TGS tickets that can be cracked offline.
9. [lookupsid](../tools/look.md): Allows you to perform [SID](../misc/sid.md) enumeration on Windows systems to gather information about existing user accounts.
10. [smbrelayx](../tools/smbrelayx.md): Similar to [ntlmrelayx](../tools/ntlmrelayx.md), it's used for SMB relay attacks, where SMB sessions are relayed to other targets.
11. [wmiexec](../tools/wmiexec.md): A tool that provides a semi-interactive shell, allowing the execution of commands via [WMI](../misc/wmi.md).
12. [smbclient](../tools/smbclient.md): A simple SMB client that allows for file and directory browsing, file uploading, downloading, and deletion on SMB shares.