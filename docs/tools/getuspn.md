Impacket's `GetUserSPNs` is a script that targets [Active Directory](../activedirectory/activedirectory.md) environments to enumerate and request [Service Principal Names (SPN)](../security/spns.md) for user accounts. This is particularly useful in [Kerberoasting](../activedirectory/roasting.md) attacks.

Kerberoasting is a type of attack against Microsoft's [Kerberos authentication](../activedirectory/kerb.md) protocol. It takes advantage of the fact that in an Active Directory environment, service accounts (accounts that are used by applications/services) often have Service Principal Names (SPNs) set. These SPNs can be queried by any authenticated user in the domain.

Once an attacker obtains a Service Principal Name for a service account, they can request a [Kerberos ticket](../activedirectory/tickets.md) for that service. This ticket is encrypted with the hash of the service account's password. The attacker can then attempt to crack this ticket offline to reveal the service account's password.

`GetUserSPNs`, part of the Impacket toolkit, automates the process of querying a domain for user accounts with SPNs set and requesting the corresponding Kerberos tickets.

An example of how `GetUserSPNs`:

```bash
python GetUserSPNs.py <DOMAIN>/<USERNAME>:<PASSWORD> -request
```

!!! info
    The output of this script will typically include the Kerberos tickets for the service accounts, which can be saved and subjected to offline cracking attempts.

