IPsec (Internet Protocol Security) is a suite of protocols for securing internet protocol (IP) communications by authenticating and encrypting each IP packet of a communication session. IPsec includes protocols for establishing mutual authentication between agents at the beginning of a session and negotiation of cryptographic keys to be used during the session.

IPsec is designed to secure data transmitted across IP networks, including the internet. It provides confidentiality, data integrity, and authentication of the data packets. IPsec encrypts the data payload of each packet, which ensures confidentiality, and it authenticates the sender, providing protection against data tampering and unauthorized access.

IPsec primarily uses two protocols:

- **Encapsulating Security Payload (ESP)**: Provides confidentiality, along with authentication and integrity.
- **Authentication Header (AH)**: Provides authentication and integrity but does not encrypt the data.

IPsec operates in two modes:

- **Transport Mode**: Encrypts and/or authenticates the data (payload) of IP packets. IP headers are not encrypted, making this mode suitable for end-to-end communication between hosts.
- **Tunnel Mode**: Encrypts and/or authenticates the entire IP packet. A new IP header is added to the packet, making this mode suitable for gateway-to-gateway communications (like site-to-site VPNs).

IPsec uses Security Associations, which are agreements on how to secure communication. SAs define the protocols and algorithms to be used for securing packet flows.

IPsec commonly uses the [Internet Key Exchange (IKE)](../protocols/ike.md) protocol to handle the negotiation of keys and the establishment of security associations.

IPsec is widely used in creating [Virtual Private Networks](../security/vpns.md) (VPNs). In a VPN, IPsec provides secure connections between remote users and networks or between different networks over the internet. IPsec policies define how traffic is to be secured. These policies determine which traffic needs to be secured and how it should be processed.