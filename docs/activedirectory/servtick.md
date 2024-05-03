In the [Kerberos authentication](../activedirectory/kerb.md) protocol, a service ticket is a key element that allows a user to access a specific network service securely. After initially authenticating with the Kerberos [Key Distribution Center (KDC)](../activedirectory/kdc.md), the user is granted a service ticket, which is then used to authenticate to the desired service within the network.

First, the user authenticates to the Kerberos [Authentication Service (AS)](../activedirectory/as.md) and receives a [TGT](../activedirectory/tgt.md). The user's client system then requests a service ticket for a specific network service from the [Ticket Granting Service (TGS)](../activedirectory/tgs.md). This request includes the TGT and the name of the service the user wants to access.

The TGS validates the TGT and, if the user is authorized to access the service, issues a service ticket. This ticket is encrypted with a key known only to the TGS and the specific service. The user presents the service ticket to the desired service. The service decrypts the ticket and, if valid, grants access to the user.

As an example, imagine a user wants to access a file server within the company network:

1. **Initial Authentication**: Alice logs into her workstation and is authenticated by the Kerberos AS. She receives a TGT.
2. **Requesting File Server Access**: When Alice tries to access FileServer1, her client system requests a service ticket from the TGS, using her TGT. The request specifies that she needs access to FileServer1.
3. **Service Ticket Issuance**: The TGS verifies Alice's TGT, confirms that she is permitted to access FileServer1, and issues a service ticket for this purpose. The ticket is encrypted with a secret key known only to the TGS and FileServer1.
4. **Accessing FileServer1**: Alice's client system presents the service ticket to FileServer1. FileServer1 decrypts the ticket, verifies it, and grants Alice access to the requested files.

