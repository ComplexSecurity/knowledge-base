Kerberoasting is a type of cyber attack that targets the [[Kerberos authentication]] protocol in Windows networks. It specifically exploits the [[Service Principal Names (SPN)|Service Principal Names (SPNs)]] used to uniquely identify service instances on the network. Attackers use Kerberoasting to crack the passwords of service accounts, which often have high privileges and are typically less monitored than user accounts.

In a Windows environment, services running under a service account can have an SPN associated with them. This SPN is used by the Kerberos protocol to authenticate the service. An attacker, who has already gained limited access to the network, enumerates the SPNs for service accounts on the domain and requests a [[Kerberos tickets|Kerberos ticket]] for each one. These tickets are encrypted using the hash of the service account's password.

The attacker extracts the Kerberos tickets from memory and then attempts to crack the encrypted tickets offline to retrieve the service account's plaintext password. This is often feasible because service account passwords are not always as strong or frequently changed. If successful in cracking a password, the attacker can impersonate the service account, potentially gaining access to sensitive areas of the network.

Imagine a company with a network where various services are running under different service accounts. One of these accounts, `svc_account`, has an associated SPN for a database service it runs:

1. An attacker with basic user privileges on the network lists all SPNs using a tool like [[SetSPN]] or [[Windows PowerShell]] commands.
2. They find the SPN associated with `svc_account` and request a service ticket for this account.
3. Once they have the service ticket, they use tools like [[tgsrepcrack]] or [[John the Ripper]] to crack the encrypted part of the ticket, which contains the hash of the `svc_account`'s password.
4. If `svc_account`'s password is weak, the attacker successfully retrieves it and gains access to the database service with the privileges of `svc_account`.



