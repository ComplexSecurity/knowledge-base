Kerberos tickets are a fundamental part of the [Kerberos](../activedirectory/kerb.md) protocol, which is a network authentication system. In a Kerberos-enabled environment, these tickets enable users to prove their identity to various network services securely and without needing to repeatedly enter their credentials.

There are two types of Kerberos tickets:

1. [Ticket Granting Ticket (TGT)](../activedirectory/tgt.md): Issued by the [Key Distribution Center](../activedirectory/kdc.md)'s [Authentication Service (AS)](../activedirectory/as.md) when a user first authenticates. The TGT is used to obtain other tickets and is encrypted with a key known only to the [Ticket Granting Service (TGS)](../activedirectory/tgs.md) and the AS.
2. [Service Ticket](../activedirectory/servtick.md): Used to access specific network services. Service tickets are obtained from the TGS using the TGT and are encrypted with a key known only to the TGS and the specific service.

When a user logs in, they present their credentials (such as a username and password) to the AS. The AS verifies these credentials and issues a TGT. To access a network service, the user's system requests a service ticket from the TGS, using the TGT to authenticate this request. The service ticket is then presented to the desired network service. The service decrypts the ticket and grants access if it is valid.

Kerberos tickets have a limited validity period, after which they expire. This limits the time window in which a ticket can be used if compromised. Tickets are encrypted, ensuring that only the intended recipient can use them. The TGT is encrypted with the TGS's key, while service tickets are encrypted with the destination service's key. The TGT allows users to obtain service tickets for different services without re-entering their credentials, enabling [SSO](../security/sso.md) within the Kerberos realm.

