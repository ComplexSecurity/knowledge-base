SMB 2 ([[Server Message Block]] 2) is a network file-sharing protocol and an updated version of the original SMB protocol. It was introduced by Microsoft in Windows Vista and Windows Server 2008. SMB 2 was developed to overcome the limitations of the older [[SMB 1]].0 protocol, particularly regarding performance, scalability, and security.

SMB 2 includes significant performance improvements over SMB 1, particularly in reducing the "chattiness" of the protocol (fewer commands and subcommands), which enhances speed and efficiency, especially in high-latency networks. It reduces the amount of overhead required in the protocol, resulting in better utilization of network bandwidth and faster file transfers.

SMB 2 is more scalable than SMB 1, supporting larger buffer sizes and a greater number of concurrent open file handles. It introduces the concept of durable file handles, which allows for a more robust handling of network disruptions and maintains file accessibility across temporary network issues.

SMB 2 includes better mechanisms for security and encryption, laying the groundwork for the more advanced security features that were fully realized in [[SMB 3]]. SMB 2 can negotiate the use of different SMB versions, which allows for compatibility and better performance between different versions of Windows.

Improved oplocks in SMB 2 enhance the caching and synchronization of shared files.

SMB 3, introduced with Windows 8 and Windows Server 2012, further extends the capabilities of SMB 2, particularly in areas like encryption, performance, and fault tolerance. Many modern Windows networks utilize SMB 3, although SMB 2 remains in use, especially in environments with a mix of older and newer Windows versions.

