mDNS (Multicast DNS) is a network protocol used for resolving hostnames to IP addresses within small networks that do not include a local name server. It is a part of the Zero-configuration networking (Zeroconf) protocol suite, allowing devices to use network services without manual setup or configuration.

mDNS enables devices on the same local network to discover each other and establish communication without the need for a central [DNS](../networking/dns.md) server. It's particularly useful in home networks, small offices, or [IoT](../terms/iot.md) (Internet of Things) environments.

Similar to traditional DNS, mDNS resolves hostnames to IP addresses. However, it operates in a smaller scope, typically limited to a single local network segment. mDNS uses multicast [UDP](../networking/udp.md) to send query messages to which all listening devices on the network can respond. A device will respond to an mDNS query only if it has the requested hostname.

Hostnames in mDNS typically end in `.local`. For example, a device named "printer" might advertise itself as `printer.local`. 

When a device needs to know the IP address of another device with a given hostname, it sends an mDNS query to a multicast address. All devices listening for mDNS queries check if the queried hostname matches their own. If there's a match, the device responds with its IP address. The querying device can then use this IP address to establish a direct connection to the responder.

mDNS is used to resolve hostnames for devices and services on local networks without the need for manual DNS configuration. Common examples include printers, file servers, and collaborative software. In IoT applications, mDNS allows devices to discover and communicate with each other on a local network without complex configuration.

