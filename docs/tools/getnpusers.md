Impacket's `GetNPUsers` is a [Python](../programming/python.md) script included in the [Impacket](../tools/impacket.md) suite that is specifically designed for querying a domain controller in a Microsoft [Active Directory](../activedirectory/activedirectory.md) environment to obtain [Kerberos Ticket Granting Tickets (TGTs)](../activedirectory/tgt.md) for accounts that do not require [Kerberos](../activedirectory/kerb.md) pre-authentication. This script is useful in the context of penetration testing, particularly for an attack known as [AS-REP Roasting](../security/asreproasting.md).

AS-REP Roasting is an attack targeting accounts in an Active Directory environment that have the "Do not require Kerberos pre-authentication" option set. When this setting is enabled for an account, it's possible to request a Kerberos TGT for the account without needing to supply a valid password. The TGT can be encrypted with weak encryption or encryption that can be cracked offline, potentially exposing the user's credentials.

`GetNPUsers` attempts to get the TGTs for those user accounts in a [[Domain Controller]] that do not require pre-authentication. The script can be executed with a list of users or can query all users in a domain.

The basic usage of `GetNPUsers` might look like this:

```bash
python GetNPUsers.py <DOMAIN>/<USERNAME> -no-pass
```

- Replace `<DOMAIN>/<USERNAME>` with the appropriate domain and username. The `-no-pass` option is used when no password is provided.
- If successful, the script will output the Kerberos TGTs for accounts not requiring pre-authentication. These TGTs can then potentially be cracked offline.

