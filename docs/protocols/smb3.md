SMB 3, the third version of the [Server Message Block](../protocols/smb.md) (SMB) protocol, is a network file sharing protocol that was introduced by Microsoft with Windows Server 2012 and Windows 8. SMB 3 brings significant improvements over its predecessors, [SMB 1](../protocols/smb1.md) and [SMB 2](../protocols/smb2.md), in terms of performance, security, and reliability. It's designed for more efficient and secure file sharing across networks, particularly in enterprise environments.

SMB 3 enhances security through features like end-to-end encryption, which secures data in transit, and pre-authentication integrity to prevent [man-in-the-middle attacks](../security/mitm.md). It introduces several performance improvements, including multichannel support, which allows SMB 3 to use multiple network connections simultaneously for higher throughput and fault tolerance.

SMB 3 includes features for network fault tolerance, like transparent failover with durable handles, helping maintain consistent file access even during network or server failures. SMB 3 is optimized for applications like [Hyper-V](../misc/hyperv.md) and [SQL Server](../databases/sqls.md), allowing them to store virtual machine and database files on SMB file shares.

[SMB Direct](../protocols/smbdir.md) uses network adapters that support [RDMA (Remote Direct Memory Access)](../misc/rdma.md) for high-speed data transfers with low latency and CPU usage. [SMB Multichannel](../protocols/smbmulti.md) allows the aggregation of network bandwidth and network fault tolerance if multiple network paths are available between the SMB client and server.

Improvements in opportunistic locking (oplocks) and the introduction of leasing improve the caching and synchronization of shared files, enhancing performance in multi-user scenarios.

SMB 3 is widely used in enterprise environments for sharing and accessing files on networked servers. Its support for Hyper-V makes it suitable for storing and accessing virtual machine files in network storage. SMB 3 can be used for storing database files in environments like SQL Server.

SMB 3 allows for secure negotiation of connections and can encrypt file transfers, making it significantly more secure against eavesdropping and tampering. Proper configuration of SMB 3 is crucial, especially in mixed environments where different versions of SMB coexist. Ensuring that clients and servers are using the most secure version of the protocol compatible with their setup is important.



