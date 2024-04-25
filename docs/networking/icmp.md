ICMP, short for Internet Control Message Protocol, is a [network layer](../networking/network.md) protocol used by network devices, including routers, to send error messages and operational information indicating success or failure when communicating with another [IP address](../networking/ipa.md). ICMP is an integral part of the Internet Protocol Suite, as defined in RFC 792.

ICMP is used for diagnosing and reporting network errors and issues. For example, if a router cannot forward an IP packet due to a problem, it might send an ICMP message back to the sender indicating the issue.

Tools like [Ping](../tools/ping.md) and [Traceroute](../tools/traceroute.md) use ICMP to test the reachability of network devices on an IP network.

1. **Types of Messages**:
   - **Echo Request and Echo Reply**: Used by the ping command to check network connectivity.
   - **Destination Unreachable**: Indicates that a network destination is unreachable.
   - **Time Exceeded**: Sent back to the source when a packet has expired (due to a TTL value reaching zero, indicating it has been in the network too long).

Unlike [Transmission Control Protocol](../networking/tcp.md) or [User Datagram Protocol|UDP](../networking/udp.md), ICMP is not used for sending and receiving data between end systems. It doesn’t carry application layer data but instead is used for control messaging.

ICMP has a version for IPv6 called ICMPv6, which, in addition to providing similar functionalities as ICMP for IPv4, also handles IPv6-specific messages, like Neighbor Discovery.
