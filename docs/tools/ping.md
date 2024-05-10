The "ping" command is a widely used network administration utility that tests the reachability of a host on an [Internet Protocol (IP)](../protocols/ip.md) network. It also measures the round-trip time for messages sent from the originating host to a destination computer and back.

The ping command sends [Internet Control Message Protocol (ICMP)](../networking/icmp.md) echo request packets to the target host and listens for ICMP echo response replies. This process helps determine whether the target host is reachable across an IP network.

Ping measures the time it takes for a packet to go from the source to the destination and back. This measurement is typically presented in milliseconds and is a key indicator of the latency or delay between the two hosts.

Ping is commonly used to troubleshoot and diagnose network connectivity issues. If the target host responds to the ping request, it confirms that the network connection between the source and destination is operational.

Ping reports errors and packet loss. If packets are lost or an error occurs (like a timeout), it suggests issues in the network such as congestion, faulty routing, or problems with the destination host.

While primarily a diagnostic tool, ping can also give a basic sense of network performance. High response times indicate potential problems with the network speed or stability.

Some systems and networks block ICMP traffic (hence, the ping command) for security reasons, as ICMP can be used for malicious purposes like network reconnaissance and [Denial-of-Service (DoS)](../security/dos.md) attacks.

Ping does not give detailed information about the nature of network issues; it only indicates whether a host is reachable.

!!! danger
    If a ping command does not receive a response, it does not necessarily mean that the host or the entire network is down. [Firewall](../security/firewall.md), network policies, or the host configuration might be set to ignore or block ICMP requests.

Hackers and pentesters use ping to identify which hosts on a network are online. By sending ICMP echo requests to different IPs on a network, they can map out which addresses are active. The response times and patterns can give insights into the network's topology and efficiency.

Different operating systems respond with different values:

- Unix/Linux - 64
- Windows - 128
- Solaris/AIX - 265

The TTL will be a reflection of this minus the number of hops it took to reach that host. If it took 8 hops to ping a Windows host for example, the TTL may be something like 120 or 119.



