SMB Direct, also known as [[Server Message Block|SMB]] over [[RDMA (Remote Direct Memory Access)]], is a feature of the Server Message Block (SMB) 3.x protocol, introduced by Microsoft. It enables the SMB protocol to operate over RDMA-capable network adapters, providing significant performance improvements for file sharing and data transfer tasks.

SMB Direct allows [[SMB 3|SMB 3.x]] to leverage the high throughput and low latency capabilities of RDMA networks, resulting in faster file transfers and improved overall performance. By using RDMA, SMB Direct offloads much of the data transfer work from the CPU to the network hardware. This reduces CPU usage and can improve the efficiency of data transfers.

RDMA technology enables direct memory-to-memory data transfers with minimal latency, which is beneficial for applications requiring fast access to network storage, such as database operations and virtualized environments. 

SMB Direct can operate over various RDMA technologies, including [[InfiniBand]], [[iWARP]] (Internet Wide Area RDMA Protocol), and [[RDMA over Converged Ethernet (RoCE)|RoCE (RDMA over Converged Ethernet)]]. With reduced CPU overhead and efficient data transfer mechanisms, SMB Direct enhances the scalability and reliability of network operations, especially in data-intensive environments.

SMB Direct is used in enterprise environments where large file shares are common, and high-speed access is required. Microsoft [[Hyper-V]] (virtualization) and [[Microsoft SQL Server|SQL Server]] (database) can leverage SMB Direct for storing and accessing virtual machine files and databases on SMB file shares, providing better performance.

Both the client and server must have RDMA-capable network adapters and operate in an environment that supports RDMA (such as InfiniBand, RoCE, or iWARP). Proper configuration of the network to support RDMA, including considerations for bandwidth and latency, is essential.

SMB Direct is supported in Windows Server 2012 and later versions, as well as in certain editions of Windows 8 and later. For SMB Direct to function, all components in the data path must support RDMA and be properly configured to work together.


