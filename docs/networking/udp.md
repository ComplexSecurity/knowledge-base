UDP, or User Datagram Protocol, is a communication protocol used across the Internet. It's part of the Internet Protocol Suite, commonly known as [TCP/IP](../networking/tcpip.md). Unlike its counterpart, [TCP](../networking/tcp.md), UDP is known for its simplicity and speed in data transmission, but this comes at the cost of reliability and ordering.

UDP is a connectionless protocol meaning that UDP does not establish a connection before sending data. Instead, it sends packets directly to the recipient without prior communications to set up special transmission channels or data paths.

However, because there's no need to establish a connection, UDP is faster and more efficient for certain types of applications. It avoids the overhead of connection establishment, maintenance, and termination, which is characteristic of TCP.

UDP does not offer error recovery. If a packet is lost, out of order, or corrupted, UDP does not resend it. This is unlike TCP, which provides extensive error checking and recovery.

With UDP, there's no mechanism to manage the flow of data between sender and receiver. This means the sender can overwhelm the receiver with too much data too quickly.

Finally, each UDP packet is independent of the other. This stateless nature means that if one packet encounters an issue in transmission, it does not affect any other packets.
