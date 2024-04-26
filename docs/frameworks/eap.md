EAP (Extensible Authentication Protocol) is a framework frequently used in network authentication. Initially developed for point-to-point connections, EAP has been extensively employed in wireless network and point-to-point authentication, particularly within the 802.1X standard for network access control.

EAP itself is not a specific authentication mechanism but a framework that supports numerous authentication methods. These methods include token cards, [Kerberos](../activedirectory/kerb.md), One-Time Passwords (OTP), smart cards, [Public Key Infrastructure (PKI)](../cryptography/pki.md), and more.

The strength of EAP lies in its flexibility. It can support new authentication methods and can be used over various transport mechanisms like wireless, [Point-to-Point Protocol (PPP)](../networking/ppp.md), and Ethernet.

EAP is widely used in wireless networks, particularly in IEEE 802.11 (Wi-Fi) through the 802.1X standard. It provides a means to securely authenticate devices and users to a wireless network.

Some common EAP authentication types include EAP-TLS ([Transport Layer Security](../cryptography/tls.md)), EAP-TTLS (Tunneled Transport Layer Security), PEAP (Protected EAP), and EAP-SIM (for SIM cards on mobile devices).

EAP-TLS is one of the most secure EAP methods, using a full [TLS handshake](../protocols/tlshand.md) to provide mutual authentication between the client and server and generate encryption keys. It requires both a server-side and a client-side certificate.

EAPoL is a version of EAP used over Ethernet ([Local Area Networks (LANs)](../networking/lans.md)) networks. It's a key component of the 802.1X authentication protocol. In many network implementations, EAP authentication messages are encapsulated within [RADIUS (Remote Authentication Dial-In User Service)](../networking/radius.md) messages and transported to an authentication server.

The security of an EAP implementation depends on the specific authentication method being used. Some methods, like EAP-TLS, offer strong security, while others may have vulnerabilities. EAP is often used in combination with other protocols to control network access. It can enforce policies such as requiring encryption, updating antivirus software, or checking for system patches before granting access.

EAP is also used in VPN ([Virtual Private Network](../security/vpns.md)) configurations and remote access services to authenticate remote users connecting to a network.
