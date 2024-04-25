"Pass the Ticket" (PtT) attacks are a type of cybersecurity threat targeting networks that use the [[Kerberos authentication]] protocol, primarily seen in Microsoft Windows environments. In a PtT attack, an attacker steals a Kerberos ticket from one machine and then uses it to gain unauthorized access to resources on another machine within the network.

The attacker first obtains a valid Kerberos ticket from a user or service account. This can be done by extracting the ticket from memory on a compromised machine using tools like [[Mimikatz]]. The stolen ticket (which can be a [[Kerberos Ticket Granting Ticket (TGT)|Ticket Granting Ticket]] or a [[service ticket]]) is then used on a different machine within the same domain. The attacker "passes" this ticket to authenticate as the ticket's original owner, bypassing the need for a password.

With the stolen ticket, the attacker can access network resources (such as file shares, servers, databases) that the ticket's original owner has rights to, potentially escalating their privileges or moving laterally within the network.

An example workflow may be:

- An attacker compromises a low-level employee's workstation and extracts Kerberos tickets from memory. They use these tickets to access a file server containing sensitive company data, impersonating the employee.
- A service account's ticket is stolen and used to gain unauthorized access to a critical server. The service account has elevated privileges, which the attacker exploits to install malware or exfiltrate data.
- After gaining initial access to a network, an attacker uses a stolen TGT to authenticate to a domain controller, allowing them to create new accounts or modify existing ones for further malicious activities.


