LLMNR (Link-Local Multicast Name Resolution) is a protocol used in modern Windows operating systems as a fallback method for host name resolution. It comes into play when [[DNS]] fails to resolve a host name, and it's used in small networks where a DNS server might not be present. LLMNR operates similarly to [[NBT-NS]] (NetBIOS Name Service), using multicast over a local subnet.

LLMNR allows hosts on the same local link (subnet) to perform name resolution without requiring a DNS server. It's used for identifying resources like computers, printers, and file shares in a local network environment. If a DNS query fails, the LLMNR multicast query is sent within the local subnet to resolve a hostname to an IP address.

LLMNR can be exploited by attackers, particularly in poisoning and spoofing attacks, due to its lack of authentication for responses. This makes it a vector for various network attacks:

1. **Spoofing and Poisoning**: An attacker can respond to LLMNR requests with false information, potentially redirecting network traffic through the attacker's machine (a [[Man-in-the-Middle (MitM) attack|man-in-the-middle attack]]).
2. **Credential Harvesting**: By responding to LLMNR requests, attackers can direct a client to authenticate to a rogue server. The attacker can then capture the authentication attempt, which typically includes hashed user credentials. Tools like [[Responder]] are commonly used to exploit LLMNR in this way.
3. [[Lateral Movement]]: Once an attacker has captured credentials, they can use them to move laterally across the network, potentially escalating privileges or accessing sensitive data.

