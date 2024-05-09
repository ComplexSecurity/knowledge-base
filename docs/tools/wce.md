Windows Credential Editor (WCE) is a security tool that's used primarily in penetration testing and forensic analyses. It is designed to extract various types of passwords and credentials from Windows operating systems.

While it shares some functionality with other well-known tools like [Mimikatz](), WCE is specifically known for its ability to harvest password hashes and plaintext passwords from memory, as well as perform [pass-the-hash attacks]().

WCE can extract plaintext passwords and [NTLM]() hashes stored in memory by the Windows authentication system. This includes active logins and session data. WCE allows attackers to use captured NTLM hashes for authenticating to other systems without needing the plaintext password. This is especially useful in lateral movement within a network.

It can obtain credentials from both 32-bit and 64-bit Windows versions and is capable of working in different Windows environments, from XP through Windows 10 and server variants.

An example usage could be for extracting passwords and hashes:

```bash
wce.exe -w
```

!!! info
    This command runs WCE to extract plaintext passwords (`-w`) from memory.

Or even for a pass-the-hash attack:

```bash
wce.exe -s <USERNAME>:<NTLM_HASH>
```

!!! info
    This uses WCE to perform a pass-the-hash attack using the specified username and NTLM hash.
