SMB Multichannel is a feature of the [Server Message Block](../protocols/smb.md) (SMB) 3.x protocol, introduced by Microsoft in Windows Server 2012 and Windows 8. It provides enhanced performance and fault tolerance in network communications for file-sharing operations. SMB Multichannel allows a single SMB session to utilize multiple network connections simultaneously.

By utilizing multiple network interfaces (NICs) or multiple connections through a single NIC, SMB Multichannel can aggregate the network bandwidth, leading to higher data transfer rates. It provides redundancy in network connections. If one network path fails, SMB Multichannel can continue the file transfer over the remaining paths, ensuring uninterrupted access to shared resources.

SMB Multichannel automatically detects and uses multiple available network paths without requiring additional configuration from the user. SMB Multichannel supports [Remote Direct Memory Access (RDMA)](../misc/rdma.md) capable network adapters. RDMA allows for high-throughput, low-latency networking with minimal CPU usage, which is especially beneficial for server applications like [Hyper-V](../misc/hyperv.md) and [SQL Server](../databases/sqls.md).

This feature enhances the overall reliability and performance of SMB file sharing, especially in environments where multiple network paths or high-speed networks are available.

A Windows server with two network cards connected to different network segments can use SMB Multichannel to provide a high-availability and high-throughput file-sharing service. If one network experiences an outage or congestion, SMB Multichannel ensures that the file-sharing operation continues over the other network.

In virtualization scenarios with Hyper-V, SMB Multichannel can be used to store and access virtual machine files, allowing for high-speed data transfers and continuous availability, even if one of the network paths fails.

SMB Multichannel is typically enabled by default on systems that support [SMB 3.x](../protocols/smb3.md). However, for optimal performance, it's important to ensure that the network environment is properly configured with multiple paths and, if possible, RDMA-capable hardware. Both the SMB client and server must support SMB 3.x for Multichannel to function. Additionally, proper network configuration and hardware support are necessary to fully realize the benefits of this feature.

