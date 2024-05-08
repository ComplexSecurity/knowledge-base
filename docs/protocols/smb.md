Server Message Block in modern language is also known as **Common Internet File System**. The system operates as an [application layer](../networking/application.md) network protocol primarily used for offering shared access to files, printers, serial ports, and other sorts of communications between nodes on a network.

For instance, on Windows, SMB can run directly over [TCP/IP](../networking/tcpip.md) without the need for NetBIOS over TCP/IP. 

Server Message Block is a [client](../terms/client.md)-[server](../terms/server.md) protocol that regulates access to files and entire directories and other network resources such as printers, routers, or interfaces released for the network. The main application area of the protocol has been the **Windows** operating system series in particular, whose network services support SMB in a downward-compatible manner - which means that devices with newer editions can easily communicate with devices that have an older Microsoft operating system installed. 

With the free software project Samba, there is also a solution that enables the use of SMB in Linux and Unix distributions and thus cross-platform communication via SMB.

An SMB server can provide arbitrary parts of its local file system as shares. Therefore the hierarchy visible to a client is partially independent of the structure on the server. Access rights are defined by Access Control Lists. 

They can be controlled in a fine-grained manner based on attributes such as execute, read and full access for individual users or user groups. The ACLs are defined based on the shares and therefore do not correspond to the rights assigned locally on the server.