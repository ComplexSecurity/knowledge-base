SNMP stands for "Simple Network Management Protocol." It’s an [application layer](../networking/application.md) protocol included in the internet protocol suite, a set of the most commonly used communication protocols online.

It is one of the most widely accepted protocols for network monitoring. SNMP is used to collect data related to network changes or to determine the status of network-connected devices. Every device within the network can be queried in real time with SNMP, [TCP](../networking/tcp.md), and other types of probes for their performance metrics. 

When thresholds for certain values are exceeded, software can alert system administrators of the issue, allowing them to drill into the data and troubleshoot a solution.

All day, traffic is ebbing and flowing across your network as users conduct transfers, browse, perform downloads, and more. SNMP talks to your network to find out information related to this network device activity. For example, it tracks bytes, [packets](../networking/packet.md), and errors transmitted and received on a router, connection speed between devices, or the number of hits a web server receives.

SNMP works by sending messages, called **protocol data units** (PDUs), to devices within your network that “speak” SNMP. These messages are called SNMP Get-Requests. Using these requests, network administrators can track virtually any data values they specify.

