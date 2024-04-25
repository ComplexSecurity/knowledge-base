[[WPA2]]-[[EAP (Extensible Authentication Protocol)|EAP]] (Wi-Fi Protected Access 2 with Extensible Authentication Protocol) is an advanced security protocol used in wireless networks, particularly in enterprise and business environments. It's a part of the WPA2 (Wi-Fi Protected Access 2) standard, which provides stronger security than its predecessor, [[WPA (Wi-Fi Protected Access)|WPA]]. WPA2-EAP is designed to give individual users unique credentials for network access, offering enhanced security features.

WPA2-EAP uses the Extensible Authentication Protocol (EAP) to authenticate each user individually, as opposed to using a single pre-shared key like in [[WPA2-PSK]]. This allows for more secure and flexible authentication mechanisms.

WPA2-EAP is primarily used in enterprise settings where individual user credentials can be managed and controlled. It is well-suited for organizations with a large number of users and complex security requirements.

Typically, WPA2-EAP works with a [[RADIUS]] (Remote Authentication Dial-In User Service) server. This server handles the authentication of users based on credentials stored in a central database.

WPA2-EAP supports various EAP methods for authentication, including EAP-TLS (Transport Layer Security), PEAP (Protected EAP), and EAP-TTLS (Tunneled Transport Layer Security). Each method offers different levels of security and deployment complexity.

WPA2-EAP provides strong encryption through the use of the [[Advanced Encryption Standard (AES)]]

This encryption ensures the privacy and integrity of data transmitted over the wireless network. Unlike WPA2-PSK, where the same encryption key is used for all devices, WPA2-EAP generates dynamic, per-session encryption keys, enhancing security, especially in environments with many users.

WPA2-EAP can be integrated with network access control systems, allowing for more granular control over network resources and user access. Methods like EAP-TLS use client and server certificates for authentication, providing a high level of security but requiring a robust [[public key infrastructure (PKI)]].

WPA2-EAP is resistant to common attacks that target wireless networks, such as dictionary attacks, [[Man-in-the-Middle (MitM) attack|man-in-the-middle attacks]], and replay attacks. For businesses and organizations that must comply with regulatory standards for data security and privacy, WPA2-EAP provides a compliant solution for wireless network security.
