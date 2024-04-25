TCP, or Transmission Control Protocol, is one of the main protocols of the Internet Protocol Suite. It is used to create a reliable, ordered, and error-checked connection between two systems on an IP network, ensuring the safe and complete transfer of data. 

TCP is fundamental to the operation of the internet, underpinning a wide variety of its applications, including web browsing, email, file transfers, and more.

It is a connection-oriented protocol meaning before data is transmitted, TCP requires that a connection be established via a TCP three-way [[handshake]]. It also provides reliable transmission, ensuring that data [[packet|packets]] are delivered to the recipient in the same order they were sent without errors.

TCP also manages the rate of data transmission between a sender and receiver to ensure that the receiver is not overwhelmed by data it can't process quick enough. It also adjusts the rate of data transmission based on congestion. If congested, TCP reduces the rate of data transfer to alleviate the congestion.

Every TCP packet also includes a checksum field to check for data integrity. The receiver uses this to verify that the packet has not been corrupted during transit.

1. **Establishing a Connection:** The TCP three-way handshake is initiated. This involves the sender sending a **SYN** (synchronize) packet, the receiver responding with a **SYN-ACK** (synchronize-acknowledge) packet, and the sender finally sending an **ACK** (acknowledge) packet.
2. **Data Transfer:** Once the connection is established, data packets are sent from the sender to the receiver. TCP numbers each packet and ensures they are delivered in the correct order.
3. **Ending a Connection:** When the data transfer is complete, the connection is terminated using a process similar to the handshake - **FIN** (finish) packets are exchanged to gracefully close the connection.

TCP is essentially the polar opposite of another [[transport layer]] protocol - [[User Datagram Protocol|UDP]].

