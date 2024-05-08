[WPA2](../protocols/wpa2.md)-PSK (Wi-Fi Protected Access 2 - [Pre-Shared Key](../cryptography/psk.md)) is an encryption standard for securing wireless computer networks. It is an enhancement of the original [WPA (Wi-Fi Protected Access)](../protocols/wpa.md) standard and is designed to provide a higher level of security. WPA2-PSK is commonly used in home and small business networks where a central authentication server is not required or practical.

In WPA2-PSK, a shared key, often referred to as the Wi-Fi password, is used for network access. This key is pre-shared among all devices that connect to the network.

WPA2-PSK uses the [Advanced Encryption Standard (AES)](../cryptography/aes.md) for data encryption, providing a significant improvement in security over the original [WEP (Wired Equivalent Privacy)](../protocols/wep.md) and [WPA](../protocols/wpa.md) standards.

WPA2-PSK is designed for simplicity, making it a popular choice for home networks and small businesses. The setup involves configuring a single shared key on the wireless access point and all devices that need to connect to it.

The security of the network depends heavily on the strength and secrecy of the pre-shared key. A strong, complex password is crucial to prevent unauthorized access. If a weak password is chosen, the network is susceptible to [brute-force attacks](../security/brute.md), where an attacker tries numerous passwords until the correct one is found.

WPA2-PSK is easy to deploy and does not require complex infrastructure or extensive technical knowledge, making it accessible for most users. Devices that are certified by the Wi-Fi Alliance for WPA2 are required to support WPA2-PSK.

WPA2-PSK is backward compatible with WPA, allowing a mixture of devices with varying levels of security capabilities. WPA2-PSK is widely adopted in personal and small business environments due to its balance of security and ease of use.

To maintain network security, it's recommended to regularly update the PSK, use a strong and complex password, and keep the router’s firmware up to date.
