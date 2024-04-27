The Ticket Granting Service (TGS) is a key component of the [Kerberos authentication](../activedirectory/kerb.md) protocol. It operates as part of the [Kerberos Key Distribution Center (KDC)](../activedirectory/kdc.md) and is responsible for issuing service tickets, which are used by clients to access various network resources and services in a secure manner.

When a user first authenticates on the network, the [Authentication Service (AS)](../activedirectory/as.md), another component of the KDC, verifies their credentials. Upon successful authentication, the AS issues a [Ticket Granting Ticket (TGT)](../activedirectory/tgt.md).

When the user wants to access a specific network service (like a file server or database), their client software sends a request to the TGS, including the TGT and the name of the service they wish to access. The TGS decrypts the TGT using its secret key. If the TGT is valid, the TGS knows that the user has been authenticated and is who they claim to be.

The TGS then creates a service ticket for the requested service. This ticket contains the user's identity and permissions and is encrypted with a key that only the TGS and the requested service know. The client receives the service ticket and presents it to the desired network service. The service decrypts the ticket, verifies the user's credentials, and grants or denies access based on the permissions in the ticket.

The TGS enhances security by ensuring that users are authenticated before accessing services and that each service access request is individually authorized. Users' credentials are not exposed to network services; instead, access is mediated through tickets issued by the TGS.

The TGS supports [single sign-on (SSO)](../security/sso.md). Once a user is initially authenticated, they can access multiple services without re-entering credentials, as long as their TGT is valid. The TGS enables scalable authentication for large numbers of users and services within an organization.

