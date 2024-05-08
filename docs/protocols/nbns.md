The NetBIOS Name Service (NBNS) is a protocol used in computer networks for name resolution of [NetBIOS](../protocols/netbios.md) network names to network addresses. It's a part of the [NetBIOS-over-TCP/IP (NBT)](../protocols/nbt.md) protocol suite and plays a role similar to that of the Domain Name System ([DNS](../networking/dns.md)) in the Internet context, but for NetBIOS names within a local area network.

NetBIOS provides a naming service where each device on the network can be identified by a unique 15-character name. The 16th character, known as the "NetBIOS suffix," indicates the service type. NBNS is responsible for translating these NetBIOS names into [IP addresses](../networking/ipa.md). When a machine on the network wants to communicate with another, it asks the NBNS to translate the NetBIOS name to an IP address.

Computers on a NetBIOS network register their names with the NBNS. Other computers on the network can query the NBNS to find the IP address associated with a particular NetBIOS name. In the absence of an NBNS, NetBIOS names can also be resolved through broadcast queries within a local subnet. In this method, a machine broadcasts a request asking the machine with the target NetBIOS name to respond with its IP address.

NBNS has been a key component in early Windows networking (especially in Windows NT and 2000 environments) before the widespread adoption of DNS and [Active Directory](../activedirectory/activedirectory.md).

NBNS, like other older protocols, has its share of security vulnerabilities, including susceptibility to spoofing and poisoning attacks. For example, an attacker might respond to a NetBIOS name query with a false IP address, redirecting traffic to an attacker-controlled machine. 

Due to security and efficiency reasons, NBNS has largely been superseded by DNS in modern networks. However, NBNS might still be found in legacy systems or in some network configurations for backward compatibility. In contemporary network configurations, it's often recommended to disable NetBIOS over TCP/IP to reduce the attack surface, especially if it's not required for legacy application compatibility.

