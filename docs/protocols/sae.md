Simultaneous Authentication of Equals (SAE) is a secure password-based authentication and key establishment protocol used primarily in Wi-Fi Protected Access 3 ([[WPA3]]). SAE was developed to replace the [[Pre-Shared Key (PSK)]] method used in [[WPA2]] and is designed to provide better security features.

SAE enhances security compared to WPA2's PSK method, particularly against offline dictionary attacks, where an attacker tries to guess the network password using databases of possible passwords.

SAE is resistant to common attacks that plagued WPA2, such as Key Reinstallation Attacks (KRACK). It is specifically designed to mitigate against these vulnerabilities. SAE is based on the Dragonfly Key Exchange, a cryptographic method that securely establishes a shared key between two parties based on a shared password.

SAE provides forward secrecy, ensuring that if a session key is compromised, previous sessions remain secure. This means that capturing one key does not enable an attacker to decrypt all past communications.

In SAE, a password is still used for network access, but the protocol provides a more secure way of handling password exchanges, reducing the risk of password interception or brute-force attacks. 

By using SAE, some of the inherent weaknesses of the Pre-Shared Key system, such as the vulnerability to offline guessing attacks, are addressed. SAE is a mandatory feature of WPA3, the latest Wi-Fi security protocol, providing stronger security measures for both personal and enterprise networks.

Despite its advanced security features, SAE is designed to be user-friendly, requiring minimal configuration from the user's perspective. While SAE is a feature of WPA3, it requires compatible hardware and software, meaning that both the Wi-Fi access point and the client devices must support WPA3 for SAE to be used.


