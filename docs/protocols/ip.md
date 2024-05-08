The Internet Protocol (IP) is a set of rules governing the format of data sent over the Internet or other networks. Essentially, IP is the principal communications protocol in the Internet protocol suite for relaying datagrams ([packets](../networking/packet.md)) across network boundaries. Its routing function enables internetworking and essentially establishes the Internet.

IP works by exchanging pieces of information called packets. A packet is a small segment of data that includes the data being sent and control information about sending and receiving it.

IP provides a unique address for each computer on the network, known as an [IP address](../networking/ipa.md). This address is used to identify the sender or receiver of information packets. There are two versions of IP in use today:

- **IPv4**: The fourth version of IP and the first to be widely deployed. IPv4 uses 32-bit addresses, allowing for 4.3 billion unique addresses.
- **IPv6**: Developed to deal with the long-anticipated problem of IPv4 address exhaustion. IPv6 uses 128-bit addresses, allowing for a significantly larger number of devices to be simultaneously connected to the Internet.

IP is responsible for routing packets from the source host to the destination host, potentially across multiple nodes and networks. IP is a connectionless protocol, meaning there's no continuous connection between the end points that are communicating. 

Each packet that travels through the Internet is treated as an independent unit of data without any relation to any other unit of data. Large data sets are broken down into smaller packets for transmission and are reassembled back into the original data set by the receiving device.

In the [[OSI model]] of computer networking, IP is in the [network layer](../networking/network.md). It operates above the data link layer and below the transport layer (which includes [TCP](../networking/tcp.md) and [UDP](../networking/udp.md)). IP does not guarantee delivery of packets, the preservation of data integrity, or the order of packet delivery. Higher-level protocols like TCP are used for reliable communication.

IP enables communication between vastly different types of devices and networks, including computers, mobile devices, and local and wide area networks. Virtually all types of network communication over the Internet use IP, making it foundational to modern digital communication.

