Responder is a network tool used for penetration testing and is particularly effective for conducting [[LLMNR]], [[NBT-NS]], and [[MDNS]] poisoning. It is designed to listen for and respond to these broadcast protocols when a system is trying to resolve a hostname on the network. Responder can capture hashed credentials transmitted across the network, which can then potentially be cracked to gain unauthorized access.

Responder listens for LLMNR (Link-Local Multicast Name Resolution), NBT-NS (NetBIOS Name Service), and MDNS (Multicast DNS) broadcasts, which occur when a hostname cannot be resolved by a [[DNS]] server. Responder then responds to these requests, pretending to be the unresolved hostname.

When a Windows computer receives a response from Responder, it often automatically sends hashed user credentials to authenticate. Responder captures these hashes. It can analyze traffic to identify and exploit systems vulnerable to these types of poisoning attacks.

In a penetration test, an ethical hacker can use Responder to listen for LLMNR, NBT-NS, and MDNS requests on a network. When a computer issues such a request (e.g., due to a typo in a network share name), Responder can respond and capture the hashed credentials sent by the computer. An example may be:

```bash
sudo responder -I eth0 -v
```

After capturing the hashed credentials, tools like [[John the Ripper]] or [[Hashcat]] can be used to crack these hashes and potentially obtain plaintext passwords. By observing the types of requests and responses on the network, an attacker can gain insights into network configurations and vulnerabilities.

