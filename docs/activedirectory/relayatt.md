In the context of penetration testing and network security, relay attacks are often associated with exploiting weaknesses in authentication protocols, particularly within [[Active Directory]] (AD) environments. These attacks can allow an attacker to gain unauthorized access to network resources, escalate privileges, or compromise network security.

One of the most prominent examples of relay attacks in networking and penetration testing is the [[NTLM Relay Attack|NTLM (NT LAN Manager) relay attack]]. [[NTLM]] is an authentication protocol used in Windows networks, and it's vulnerable to relay attacks under certain conditions.

This is how NTLM Relay attacks work:

1. **Capture Authentication Request**: The attacker captures an NTLM authentication request from a client. This can be done using tools like [[Relay Attacks]] [[responder]], which tricks clients into sending their NTLM authentication requests to the attacker's machine.
2. **Relay to Another Service**: The attacker then relays this captured authentication request to another server or service on the network. If this target server accepts the relayed authentication, the attacker gains access to the server with the credentials of the victim client.
3. **Access Network Resources**: The attacker can potentially access or modify network resources, execute commands, or escalate privileges depending on the level of access of the compromised account.

Some example tools include:

- Impacket's [[ntlmrelayx]]: A tool that can perform NTLM relay attacks by relaying NTLM authentication requests to a specified target. It can also automatically execute commands or exploit known vulnerabilities upon successful relay.
- Responder: A tool for [[LLMNR]], [[NBT-NS]], and [[MDNS]] poisoning, which can force clients to send their authentication requests to the attacker’s machine, facilitating NTLM relay attacks.

