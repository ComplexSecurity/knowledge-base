Impacket's `lookupsid` is a tool that forms part of the [[Impacket]] suite of [[Python]] classes for working with network protocols. This particular tool is designed for [[Windows SID (Security Identifier)]] enumeration. It is useful in penetration testing and network security assessments for gathering information about Windows user accounts and their corresponding SIDs on a networked system.

`lookupsid` allows you to enumerate user SIDs (Security Identifiers) and group SIDs on a Windows system. Each user account and group account on a Windows system has a unique SID. By obtaining the SIDs, you can gather information about existing user accounts, which can be valuable in understanding the network's structure and potential attack vectors. The tool makes use of SMB ([[Server Message Block]]) protocol for communication, a standard protocol used in Windows networking.

An example of how `lookupsid` might be used in a penetration testing scenario. This command-line example assumes you have the necessary network access and permissions:

```bash
python lookupsid.py <DOMAIN>/<USERNAME>:<PASSWORD>@<TARGET_IP>
```

!!! info
    `lookupsid` will then attempt to connect to the target machine and enumerate SIDs. The output typically includes a list of user names and their corresponding SIDs, along with any groups and their SIDs.

