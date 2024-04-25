A port is a virtual point where network connections start and end. Ports are software-based and managed by a computer's operating system. Each port is associated with a specific process or service and there are [default ports](../networking/defaultports.md) for common services.

Ports allow computers to easily differentiate between different kinds of traffic: emails go to a different port than webpages, for instance, even though both reach a computer over the same Internet connection.

Ports are standardized across all network-connected devices, with each port assigned a number. While [IP addresses](../networking/ipa.md) enable messages to go to and from specific devices, port numbers allow targeting of specific services or applications within those devices.

Ports are a [transport layer](../networking/transport.md) concept. Only a transport protocol such as the [Transmission Control Protocol](../networking/tcp.md) or [User Datagram Protocol](../networking/udp.md) can indicate which port a packet should go to.

!!! info
There are 65,535 possible port numbers, although not all are in common use
