Impacket's `GetUserSPNs` is a script that targets [[Active Directory]] environments to enumerate and request [[Service Principal Names (SPN)]] for user accounts. This is particularly useful in [[Kerberoasting]] attacks.

Kerberoasting is a type of attack against Microsoft's [[Kerberos authentication]] protocol. It takes advantage of the fact that in an Active Directory environment, service accounts (accounts that are used by applications/services) often have Service Principal Names (SPNs) set. These SPNs can be queried by any authenticated user in the domain.

Once an attacker obtains a Service Principal Name for a service account, they can request a [[Kerberos Tickets|Kerberos ticket]] for that service. This ticket is encrypted with the hash of the service account's password. The attacker can then attempt to crack this ticket offline to reveal the service account's password.

`GetUserSPNs`, part of the Impacket toolkit, automates the process of querying a domain for user accounts with SPNs set and requesting the corresponding Kerberos tickets.

An example of how `GetUserSPNs`:

```bash
python GetUserSPNs.py <DOMAIN>/<USERNAME>:<PASSWORD> -request
```

!!! info
    The output of this script will typically include the Kerberos tickets for the service accounts, which can be saved and subjected to offline cracking attempts.

