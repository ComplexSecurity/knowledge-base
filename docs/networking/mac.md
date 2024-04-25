A MAC (Media Access Control) address is a unique identifier assigned to network interfaces for communications on the physical network segment. It's a fundamental element in the architecture of networked devices and plays a critical role in network communications, particularly at the [data link layer (Layer 2)](../networking/datalink.md) of the [OSI model](../networking/osimodel.md).

A MAC address is typically a 48-bit (6-byte) number. It's commonly written in hexadecimal format and separated by colons or hyphens, like `00:1A:2B:3C:4D:5E`. Each MAC address is meant to be globally unique. It's pre-assigned to a network interface card (NIC) or a similar device by the manufacturer.

The MAC address is divided into two parts:

- **Organizationally Unique Identifier (OUI)**: The first three bytes represent the OUI, which identifies the manufacturer or vendor of the device.
- **Device Identifier**: The remaining bytes are assigned by the manufacturer and serve to uniquely identify the network interface.

In a [Local Area Networks (LANs)](../networking/lans.md), devices use MAC addresses to identify and communicate with each other. MAC addresses operate at the data link layer of the OSI model, facilitating the transfer of data between physically connected network devices. MAC addresses are used in Ethernet and Wi-Fi networks. Each Ethernet or Wi-Fi interface in a computer, smartphone, router, or other network devices has a unique MAC address.

Network switches use MAC addresses to forward data to the correct device on a LAN. The [Address Resolution Protocol (ARP)](../networking/arp.md) maps [IP addresses](../networking/ipa.md) to MAC addresses, enabling proper routing of data in a network. MAC addresses are sometimes used in network access control and filtering, although they can be spoofed (falsely imitated).
