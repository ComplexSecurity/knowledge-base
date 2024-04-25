NetBIOS (Network Basic Input/Output System) is an older networking protocol used to enable communication between applications on different computers within a [[Local Area Networks (LANs)|local area network (LAN)]]. Originally developed in the 1980s for early IBM networks, NetBIOS became widely used in early Windows networks for local network communication and resource sharing.

NetBIOS provides a naming service that allows computers to register and resolve friendly names (up to 15 characters long). These names are used to identify and access network resources like computers, printers, and other devices. It enables the establishment and management of sessions between network devices for communication. This includes connecting, sending, receiving, and disconnecting sessions.

NetBIOS supports connectionless communication by sending and receiving datagrams, which are essentially broadcast messages sent to all devices on the network or directed to a specific NetBIOS name.

Some places where it is still used include:

- **File and Printer Sharing**: In Windows networks, NetBIOS was commonly used for file and printer sharing.
- **Network Browsing**: It was used for browsing networked computers and their shared resources in a LAN.
- **Integration with SMB Protocol**: NetBIOS was often used in conjunction with the [[Server Message Block]] (SMB) protocol for providing shared access to files, printers, and other network resources.

With the evolution of networking, particularly with the adoption of [[TCP-IP|TCP/IP]] as the standard networking protocol, the functions of NetBIOS have largely been replaced by more modern protocols like [[DNS]] and [[Dynamic Host Configuration Protocol (DHCP)|DHCP]].

Even though pure NetBIOS is rarely used now, its functionality was extended over TCP/IP networks, known as [[NetBIOS over TCP-IP (NBT)|NetBIOS over TCP/IP (NBT)]]. NetBIOS is known for its security weaknesses, making networks vulnerable to various attacks like name resolution poisoning and unauthorized access. Modern networks generally avoid using NetBIOS or tightly control its usage.

>[!important]
>While largely obsolete, NetBIOS might still be found in some legacy systems or specific network configurations for compatibility reasons.

