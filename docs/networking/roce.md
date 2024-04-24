RDMA over Converged Ethernet (RoCE) is a network protocol that allows [Remote Direct Memory Access (RDMA)]() over an Ethernet network. RoCE leverages the high throughput and low latency capabilities of RDMA, enabling efficient data transfers between servers and storage systems in data centers. It's particularly beneficial in environments where performance and low CPU overhead are critical.

RoCE allows data to be transferred directly between the memory of two machines over Ethernet, bypassing the operating system's network stack. This results in lower latency and higher throughput.

Since data transfer operations are offloaded to the network hardware, RoCE reduces the CPU overhead that would typically be required for processing network packets. RoCE is suitable for high-performance computing (HPC), storage (like NVMe over Fabrics), and enterprise data center applications due to its efficiency and speed.

There are two versions of RoCE:

- RoCE v1 operates over any standard Ethernet infrastructure.
- RoCE v2 is an extension of RoCE that operates over [Layer 3 (IP-routed) networks](network.md), increasing deployment flexibility and scalability.

RoCE requires a properly configured network that can support lossless Ethernet, typically with Priority Flow Control (PFC) and Enhanced Transmission Selection (ETS) as part of [Data Center Bridging](datacenterbridging.md) (DCB) extensions. RoCE requires network interface cards (NICs) and switches that support RDMA over Ethernet.

RoCE v1 operates at Layer 2 ([Data Link Layer](datalink.md)), which may be simpler in configuration but is limited to a single Ethernet broadcast domain. RoCE v2 operates at Layer 3 (IP layer), allowing for routing over IP networks but may require more complex configuration.

