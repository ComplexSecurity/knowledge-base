AS-REP Roasting is a type of attack targeting [Kerberos authentication]() in Windows [Active Directory]() (AD) environments. This attack exploits a vulnerability in the way Kerberos handles pre-authentication, specifically targeting accounts configured not to require pre-authentication.

In a typical Kerberos setup, when a user logs in, their client requests an "[Authentication Service Response]()" (AS-REP) from the [Kerberos Key Distribution Center (KDC)](). Normally, this request includes pre-authentication data, proving the user's identity by encrypting the timestamp with their password hash. The KDC decrypts this to verify the user's identity before sending the AS-REP.

Some accounts, however, may be configured without the requirement for pre-authentication. This is sometimes done for backward compatibility or specific configuration scenarios. An attacker can request AS-REP tickets for accounts without pre-authentication. The KDC will return encrypted data that can be cracked offline to reveal the user's password.

Using tools like [GetNPUsers]() from [Impacket](), an attacker enumerates user accounts in an AD domain that are set not to require pre-authentication:

```bash
GetNPUsers.py <Domain>/<User> -no-pass -usersfile users.txt
```

The tool requests AS-REP tickets for these accounts. The KDC responds with encrypted tickets. The attacker uses [Password Cracking|password-cracking]() tools like [John the Ripper]() or [Hashcat]() to crack these tickets and potentially recover users' passwords.

