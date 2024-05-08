  
ARP Poisoning, also known as ARP Spoofing, is a type of cyber attack carried out over a [Local Area Networks (LANs)|local area network (LAN]()) that involves sending falsified [Address Resolution Protocol (ARP)|ARP (Address Resolution Protocol)]() messages onto the network. This attack exploits the lack of authentication in the ARP protocol and is used to associate the attacker's [MAC Address|MAC (Media Access Control) address]() with the [IP address]() of another host, such as the default gateway or a specific computer on the network.

Under normal circumstances, when a device wants to communicate with another device on the network, it sends an ARP request to determine the MAC address associated with the desired IP address. The device with that IP address replies with its MAC address. 

In ARP poisoning, the attacker sends forged ARP reply messages to a target host (or hosts) on the network. These replies falsely tell the target device(s) that the attacker's MAC address corresponds to the IP address of another important host on the network, such as the gateway.

As a result, the target device(s) send data intended for that important host (like the gateway) to the attacker instead. The attacker can then intercept, modify, or block this data before potentially forwarding it to the intended host, thus executing a [man-in-the-middle (MITM) attack]().

The attacker can eavesdrop on network traffic, capturing sensitive information such as login credentials and financial data. By intercepting and modifying data, attackers can take over sessions, such as web sessions, to gain unauthorized access to web applications. By disrupting the network communication, the attacker can render network services unavailable. ARP poisoning can lead to network slowdowns and instability due to incorrect ARP mappings.

