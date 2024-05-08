An NTLM Relay attack is a type of cybersecurity attack in which an attacker intercepts and relays [NTLM]() (New Technology LAN Manager) authentication requests to access network resources. This attack exploits the NTLM protocol, which is used for authentication in Windows networks.

The attacker positions themselves in the network to intercept an NTLM authentication request from a client (user or computer). This is often achieved through techniques like [ARP poisoning]() or by exploiting protocols like [LLMNR]()/[NBT-NS]() that lack server authentication. The intercepted NTLM authentication request, which includes the user's credentials in a hashed form, is then forwarded (or "relayed") to another server within the network.

The target server processes the forwarded request as a legitimate attempt to authenticate and grants access based on the relayed credentials. The attacker gains access to the server or service, impersonating the user whose credentials were relayed.

Some examples of attacks may include:

- **Accessing File Shares**: An attacker intercepts an NTLM authentication request from a user and relays it to a file server. The server grants access, and the attacker can read, modify, or delete files on the share.
- **Compromising a Web Server**: NTLM credentials are intercepted and relayed to a web server in the network. The attacker gains access to restricted web resources or administrative interfaces.

For mitigation:

- **Disable NTLM Authentication**: Where possible, replace NTLM with more secure protocols like [NTLM Relay Attack]().
- Use [SMB Signing](): Enabling [SMB Signing]() can prevent NTLM Relay attacks on SMB ([Server Message Block]()) protocols, as it requires each packet to be signed by the client's session key.
- Enable [EPA (Extended Protection for Authentication)](): EPA helps prevent NTLM Relay attacks by binding the authentication process to the [TLS]() (Transport Layer Security) session where it originated.
- **Network Segmentation**: Properly segmenting the network can limit the ability of an attacker to relay credentials to sensitive parts of the network.
- **Patching and Updates**: Ensure all systems are patched and updated, particularly regarding any security updates related to NTLM.

