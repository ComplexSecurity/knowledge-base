[WPA](../protocols/wpa.md)-[EAP](../frameworks/eap.md) (Wi-Fi Protected Access with Extensible Authentication Protocol) is a security protocol used in wireless networks. It's part of the WPA standard, which was developed to secure wireless computer networks. WPA-EAP is particularly designed for use in enterprise environments, offering advanced authentication methods that go beyond what's provided in [WPA-PSK](../protocols/wpa-psk.md) (Pre-Shared Key).

WPA-EAP provides a framework that supports various advanced and secure authentication methods, such as EAP-TLS (Transport Layer Security), PEAP (Protected EAP), and EAP-TTLS (Tunneled Transport Layer Security). These methods allow for more secure authentication mechanisms than a simple pre-shared key.

WPA-EAP is widely used in enterprise settings where user authentication can be centrally managed and controlled. It is well-suited for organizations with a large number of users and where user credentials need to be closely managed.

WPA-EAP typically works with a [RADIUS](../networking/radius.md) (Remote Authentication Dial-In User Service) server that centrally manages authentication for all users. When a user tries to connect to the network, the access point communicates with the RADIUS server to authenticate the user.

Various EAP methods offer different levels of security and deployment complexity. For example, EAP-TLS is one of the most secure methods but requires a certificate for each client. Other methods like PEAP and EAP-TTLS provide a balance between security and ease of deployment.

With WPA-EAP, encryption keys are dynamically generated and can be unique for each user, adding an extra layer of security compared to [WPA-PSK](../protocols/wpa-psk.md), where every user shares the same key.

Many EAP methods used with WPA-EAP provide mutual authentication, where both the client and the server authenticate each other. This prevents rogue access points from capturing credentials. WPA-EAP uses strong encryption mechanisms (like [TKIP](../cryptography/tkip.md) or [AES](../cryptography/aes.md)) to protect the data over the wireless network.

Integration with enterprise systems allows network policies to be enforced more effectively. For instance, network access can be tied to a user's employment status. WPA-EAP scales well for large networks, providing efficient management of authentication credentials and allowing for changes without needing to reconfigure each client.
