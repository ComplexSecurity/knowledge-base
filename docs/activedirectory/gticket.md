A Golden Ticket is a term used in cybersecurity to describe a specific type of attack against Microsoft Windows [Active Directory](../activedirectory/activedirectory.md) systems. This attack exploits the [Kerberos authentication](../activedirectory/kerb.md) protocol and involves the creation of a forged [Ticket Granting Ticket (TGT)](../activedirectory/tgt.md).

To create a Golden Ticket, an attacker first needs to gain access to the [Key Distribution Center (KDC)](../activedirectory/kdc.md), specifically the domain controller in an Active Directory environment. The primary target is the [NTLM](../security/ntlm.md) hash of the `krbtgt` account, which is used by the domain controller to encrypt and sign all TGTs.

With the `krbtgt` account’s NTLM hash, the attacker can create a valid, forged TGT, commonly referred to as a Golden Ticket. This ticket can grant the attacker unrestricted access to any service within the domain. 

The Golden Ticket can be used to authenticate as any user (including domain administrators), to any service that uses Kerberos. It effectively allows the attacker to maintain persistence within the network and gain access to critical resources and data.

An example workflow may be:

- An attacker gains administrative access to a domain controller.
- They extract the NTLM hash of the `krbtgt` account using tools like [Mimikatz](../tools/mimi.md).
- The attacker generates a Golden Ticket using the extracted hash, granting them administrator-level access to the network.
- Using this Golden Ticket, they can access sensitive data, deploy malware, create new accounts, or carry out other malicious activities without being detected.

