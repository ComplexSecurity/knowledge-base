NetBIOS over TCP/IP (NBT) is a networking protocol that allows older [NetBIOS](../protocols/netbios.md) services to be used over modern [TCP/IP](../networking/tcpip.md) networks. NetBIOS (Network Basic Input/Output System) was developed in the 1980s for early LAN (Local Area Network) systems to enable communication between applications on different computers.

It uses 3 ports:

- **Name Service (137)** - NBT uses this service for name registration and resolution. It allows a NetBIOS name (a 16-character identifier for a networked device) to be associated with an IP address. Name resolution can be done via broadcasting or a [NetBIOS Name Server (NBNS)](../protocols/nbns.md), like [WINS](../protocols/wins.md) in Windows.
- **Datagram Service (138)** - This service provides connectionless communication. It's used for sending and receiving NetBIOS datagrams, which are typically used for one-to-many communications.
- **Session Service (139)** - This service allows the establishment of NetBIOS sessions for communication between two devices. It's used for reliable, connection-oriented communication, often employed for file and printer sharing in Windows networks.

NBT can be vulnerable to various types of attacks, such as NetBIOS name spoofing or [session hijacking](../security/sesshij.md). It is susceptible to security issues inherent in the older NetBIOS protocol. The broadcasting nature of NetBIOS name resolution can inadvertently expose network information that can be exploited by attackers. Modern Windows networks often do not require NetBIOS. It is generally recommended to disable NBT if it's not needed, to reduce the attack surface.

