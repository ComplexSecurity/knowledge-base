RADIUS (Remote Authentication Dial-In User Service) is a networking protocol that provides centralized [[Authentication, Authorization, and Accounting (AAA)]] management for users who connect and use a network service. RADIUS is widely used in various network environments, including remote access to networks, wireless networks, and Internet service providers.

RADIUS manages network access by authenticating users when they attempt to connect to the network. It verifies user credentials against a central database before granting access. After authentication, RADIUS determines what level of access and network privileges the user should have. This can include details like [[IP address]] assignment, network service access, and any other restrictions or permissions.

RADIUS keeps track of users' network usage data, such as time logged in, amount of data transferred, and other usage statistics. This information is useful for billing, auditing, and monitoring purposes. 

RADIUS operates on a client-server model, where the RADIUS server is responsible for authentication, authorization, and accounting, and the client is typically network hardware like a router, switch, or wireless access point.

RADIUS is commonly used by Internet Service Providers (ISPs) for managing access to internet services, as well as by enterprises for managing access to internal networks, especially for remote users.

RADIUS supports a range of authentication methods, including username and password, tokens, and certificates. While RADIUS encrypts user passwords in transit, the rest of the RADIUS packet is not encrypted, which can be a security concern. Protocols like IPsec are sometimes used alongside RADIUS for enhanced security.

RADIUS can be extended with vendor-specific attributes (VSAs), allowing vendors to include additional information in RADIUS messages that are specific to their equipment.

RADIUS can integrate with various directory services like [[Lightweight Directory Access Protocol|LDAP]] or [[Active Directory]], allowing for centralized management of user credentials and policies.



