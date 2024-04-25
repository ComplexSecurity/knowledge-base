Impacket's `secretsdump` is a powerful tool in the [[Impacket]] suite designed to extract various types of credentials from Windows systems. It's commonly used in penetration testing and cybersecurity assessments to extract sensitive information from compromised machines.

`secretsdump` can extract [[NTLM]] password hashes from the Security Account Manager ([[SAM]]) database found on Windows systems. These hashes can be cracked offline to potentially reveal user passwords. The tool can extract [[LSA (Local Security Authority)]] secrets, which might include stored credentials for services and applications.

It can also retrieve cached domain credentials stored on the system, which are useful in environments where machines frequently authenticate with a [[Domain Controller|domain controller]]. In a domain environment, `secretsdump` can be used to extract credentials from an [[Active Directory]] Domain Controller, including NTLM hashes of all domain users.

The tool can extract Domain backup keys used in [[DPAPI (Data Protection API)]] system, which can be used to decrypt other DPAPI-protected data.

A basic example may be:

```bash
python secretsdump.py <DOMAIN>/<USERNAME>:<PASSWORD>@<TARGET_IP>
```

!!! info
    The output will typically include a list of user accounts and their corresponding NTLM hashes, among other information.

