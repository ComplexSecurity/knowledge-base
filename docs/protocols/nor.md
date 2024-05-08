NFS over RDMA (Remote Direct Memory Access) is an implementation of the [Network File System (NFS)](../protocols/nfs.md) protocol that utilizes [RDMA](../misc/rdma.md) technology for data transfer. This combination enhances NFS by providing a more efficient and high-performance way to access remote file systems over a network.

NFS is a distributed file system protocol that allows a user on a client computer to access files over a network in the same way they would access local storage. It's widely used in Unix/Linux environments.  RDMA is a technology that enables the direct transfer of data from the memory of one computer to another without involving the CPU, cache, or operating system of either system. It significantly reduces latency and increases throughput.

By leveraging RDMA, NFS over RDMA provides higher throughput and lower latency compared to traditional NFS implementations over [TCP/IP](../networking/tcpip.md). Since RDMA offloads the work of data transfer to the network hardware, it reduces CPU usage on both the client and server, making data transfers more efficient. 

RDMA's direct memory access capability significantly reduces the number of data copies and context switches, which lowers latency. NFS over RDMA can handle a larger number of simultaneous connections and higher volumes of data transfer with less impact on system resources.

Both the NFS server and client must have RDMA-capable network adapters (RNICs) and operate in an environment that supports RDMA (like [InfiniBand](../networking/infiniband.md) or [iWARP](../networking/iwarp.md)). The operating system and NFS implementation must support NFS over RDMA. Many Unix/Linux distributions provide this support.

Proper configuration of network interfaces, NFS settings, and RDMA parameters is necessary to ensure optimal performance and stability.