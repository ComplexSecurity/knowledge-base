iWARP (Internet Wide Area RDMA Protocol) is a network protocol that enables [Remote Direct Memory Access (RDMA)](../misc/rdma.md) over standard [TCP/IP](../networking/tcpip.md) networks. It extends the capabilities of RDMA, traditionally confined to high-speed [InfiniBand](../networking/infiniband.md) networks, to Ethernet-based networks.

iWARP allows for high-throughput, low-latency data transfers across network environments using the familiar and ubiquitous TCP/IP protocol stack.

iWARP facilitates RDMA operations over standard Ethernet networks, which are more common and widespread than InfiniBand networks, especially in enterprise data centers. Since iWARP operates over TCP/IP, it can be deployed on existing Ethernet infrastructure without requiring specialized network switches. This makes it relatively easy to implement in many existing network environments.

iWARP provides the low latency and high bandwidth benefits of RDMA, making it suitable for performance-critical applications like high-performance computing (HPC), storage area networks (SANs), and data center operations.

By offloading data transfer operations from the CPU to the network interface card (NIC), iWARP reduces CPU usage and improves overall system performance. iWARP includes congestion management capabilities inherent in [Transmission Control Protocol](../networking/tcp.md), making it robust in diverse network conditions, including in [Wide Area Network (WANs)](../networking/wans.md).

InfiniBand is another RDMA technology offering high performance but requires dedicated InfiniBand infrastructure. iWARP, on the other hand, operates over standard Ethernet.

[RDMA over Converged Ethernet (RoCE)](../networking/roce.md) also allows RDMA over Ethernet but requires a lossless Ethernet environment, which can involve additional configuration and equipment (like [Data Center Bridging](../networking/datacenterbridging.md), DCB). iWARP, leveraging TCP/IP, can operate over standard Ethernet without these additional requirements.
