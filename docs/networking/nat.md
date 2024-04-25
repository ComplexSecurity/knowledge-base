NAT (Network Address Translation) is a method used in networking to modify network address information in IP packet headers while they are in transit across a traffic routing device. It is commonly used in routers and [Firewall](../security/firewall.md).

One of the primary purposes of NAT is to conserve global [IP Address](../networking/ipa.md) by allowing multiple devices on a private network to be mapped to a single public IP address. This is particularly important given the limited number of IPv4 addresses available.

Types of NAT:

- **Static NAT**: Maps an unregistered IP address to a registered IP address on a one-to-one basis.
- **Dynamic NAT**: Maps an unregistered IP address to a registered IP address from a group of available addresses.
- **Port Address Translation (PAT)**: Also known as "NAT overload", PAT maps multiple unregistered IP addresses to a single registered IP address by using different ports.

NAT is often used to enable 'IP masquerading', where all devices on a private network appear to the outside world to have the same IP address (the router’s public IP address). This is commonly used in home and small business networks.

By hiding internal IP addresses, NAT can add a layer of security to the network. External users see only the public IP address, making it more difficult to target specific devices within the local network.

NAT is typically performed by routers, which are set up to translate the private IP addresses of devices within the network to a public address for internet communication. Some applications and protocols that require peer-to-peer connections, like VoIP and online gaming, can be disrupted by NAT, as it can prevent direct communication between devices.

Various techniques, like UPnP (Universal Plug and Play) and STUN (Session Traversal Utilities for NAT), are used to overcome the limitations imposed by NAT, especially in peer-to-peer communications.

NAT is predominantly a solution for IPv4 networks. IPv6, with its larger address space, reduces the need for NAT, though NAT for IPv6 does exist. Many Internet Service Providers (ISPs) use NAT to manage the limited number of IPv4 addresses available, especially as the world transitions more towards IPv6.
