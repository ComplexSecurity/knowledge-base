Kerberos is a computer network security protocol that authenticates service requests between two or more trusted hosts across an untrusted network, like the internet. It is now a default authorization technology in Microsoft Windows and is also implemented in other operating systems like Apple OS, FreeBSD, UNIX, and Linux.

Kerberos employs secret-key cryptography and a trusted third party, the Key Distribution Center (KDC), to authenticate client-server applications and verify user identities. The **KDC** provides authentication and ticket-granting services, issuing "tickets" for secure identity verification. This process uses shared secret cryptography, protecting against eavesdropping and replay attacks.

Kerberos is employed heavily on secure systems that depend on reliable auditing and authentication features. Kerberos is used in Posix authentication, and [Active Directory](../activedirectory/activedirectory.md), [NFS](../protocols/nfs.md), and [Samba](../protocols/smb.md). It's also an alternative authentication system to [SSH](../protocols/ssh.md), [POP](../protocols/pop.md), and [SMTP](../protocols/smtp.md).

Kerberos protocol represents the following three things:

- Client
- Network Resource (Application server)
- Key Distribution Center (KDC)

With these three components, Kerberos enables trusted host authentication over untrusted networks. Kerberos ensures that only authorized users can access the network resources. Additionally, it provides AAA security: **Authentication**, **Authorization**, and **Accounting**.  

In Kerberos, KDC grants tickets. These allow different hosts to prove their identity. In addition, the developers intended for Kerberos' authentication that supports authorizations. That means a client authenticated by Kerberos also has access.

Kerberos Authentication Protocols works by the following:

- **Authentication Server Request**: The client requests authentication from KDC. This authentication request would be in plain text. 
- **Authentication Server Response**: KDC sends a TGT and a session key if the client exists in the database. If the client is not in the database, the authentication fails.  
- **Service Ticket Request**: The client asks for the service ticket along with the TGT sent earlier by the KDC. 
- **Service Ticket Response**: KDC sends the ticket encrypted with the session key. The client can use the session key sent earlier by KDC to decrypt the service ticket.
- **Application Server Request**: The client requests the application server for access using the service ticket. 
- **Application Server Response**: The application server authenticates the client. It sends a ticket that will grant access to that particular service. 

The service ticket has a specific expiry time. You can use the same session ticket to access services until it expires. The default lifetime of a Kerberos ticket is 600 minutes.
