The Network Time Protocol (NTP) is an [application layer](../networking/application.md) protocol in the [TCP/IP](../networking/tcpip.md) protocol suite. It is used to synchronize the clock between the [client](../terms/client.md) and the [server](../terms/server.md) to provide high-precision time correction. 

The NTP server receives accurate Coordinated Universal Time (UTC) from an authoritative clock source, such as an atomic clock or GPS. Then, the NTP client requests and receives time from the NTP server.  

NTP relies on [User Datagram Protocol](../networking/udp.md) (UDP) port 123.