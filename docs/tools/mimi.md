Mimikatz is a well-known and powerful tool in the field of cybersecurity, particularly used in penetration testing and digital forensics. Developed by Benjamin Delpy (`gentilkiwi`), Mimikatz is designed to gather and manipulate credentials and other security-related information from Windows systems. It's famous for its ability to extract plaintext passwords, hash values, PIN codes, and [[Kerberos Tickets]] from memory.

Mimikatz can extract plaintext passwords from memory, particularly from the [[LSASS (Local Security Authority Subsystem Service)]] process in Windows. It allows for the extraction and use of [[NTLM]] hashes and Kerberos tickets, enabling [[pass-the-hash attacks]] or [[Pass-the-Ticket Attacks]] for [[lateral movement]] in networks.

Mimikatz can create a "[[Golden Ticket]]," which is a forged [[Kerberos Ticket Granting Ticket (TGT)]] that provides broad access to a network. It can interact with various Windows authentication protocols, such as NTLM, [[Kerberos authentication|Kerberos]], and more, for testing and exploitation.

Some example uses include extracting plaintext passwords:

```bash
mimikatz # sekurlsa::logonpasswords
```

>[!info]
>This command lists the plaintext passwords and hashes of logged-in accounts.

Or creating golden tickets:

```bash
mimikatz # kerberos::golden /user:Administrator /domain:<DOMAIN> /sid:<DOMAIN_SID> /krbtgt:<KRBTGT_HASH> /id:500
```

>[!info]
>This creates a Golden Ticket for the domain administrator. The required parameters are the domain name, domain [[Windows SID (Security Identifier)|SID]], and krbtgt account hash.

Or extracting NTLM hashes:

```bash
mimikatz # lsadump::sam
```

>[!info]
>This dumps the [[SAM]] database containing NTLM hashes of local accounts.






