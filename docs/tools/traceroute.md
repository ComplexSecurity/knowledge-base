Traceroute is a network diagnostic tool used for tracking the path that an [Internet Protocol (IP)](../protocols/ip.md) packet takes from its source to its destination. It reports the [IP address](../networking/ipa.md) of all the [Routers](../networking/routers.md) it traverses until it reaches the destination or times out. Traceroute is used to diagnose network routing issues and to gain insight into the path network traffic takes to reach its destination. 

Traceroute is used to diagnose network connectivity issues, such as delays or failures in data transmission. It helps in understanding the path (route) taken by packets across a network, which can be crucial for troubleshooting network issues or for performance analysis.

Traceroute sends a sequence of [Internet Control Message Protocol (ICMP)](../networking/icmp.md) echo request packets to the destination with incrementally increasing Time-To-Live (TTL) field values. The TTL value limits the number of hops a packet can take.

Each router along the path decrements the TTL value of the packet by one, and when the TTL value reaches zero, the router drops the packet and sends back an ICMP "Time Exceeded" message to the sender.

By incrementing the TTL and receiving Time Exceeded messages, traceroute can determine the path the packets take to reach the destination.

The output of traceroute shows a list of hops (routers or switches) that the packets traverse on their way to the destination. Along with the address of each hop, traceroute usually displays the time taken to reach that hop, often measured in milliseconds.

Some routers and [firewalls](../security/firewall.md) are configured to block ICMP packets or limit their processing, which can cause traceroute to give incomplete or misleading results. Traceroute only shows the path from the source to the destination at the time it's run. Network routes can dynamically change, so the path might be different at different times.

