DNS tunneling is a technique used to encode the data of other programs or protocols in [DNS](dns.md) queries and responses. It leverages the DNS protocol, which is used to resolve domain names into IP addresses, as a carrier for data transmission, often to bypass network security measures that do not adequately monitor and filter DNS traffic.

Data that needs to be transferred is broken down and encapsulated in DNS query packets. These packets are sent to a DNS server that is controlled by the attacker or penetration tester. The attacker's DNS server receives the query, decodes the data, processes it, and responds accordingly. The response itself can also be used to carry data back. 

Because DNS is a necessary and trusted protocol, many networks do not inspect DNS packets as closely as other types of traffic, making DNS tunneling an effective method for bypassing [Firewall]() and network security systems.

DNS tunneling can be used to:

1. Simulate Exfiltration: Test the network's ability to detect and prevent data exfiltration. Penetration testers use DNS tunneling to demonstrate how an attacker could covertly move data in and out of the network.
2. Bypass Network Segmentation: Test the effectiveness of network segmentation and firewall rules. Since DNS is often allowed through network perimeters, it can be used to communicate with external servers even from isolated network segments.
3. Command and Control (C2) Communications: Simulate [Command and Control (C2)]() channels that use DNS tunneling to control compromised systems without being detected by traditional security defenses.

Some examples may include:

- [Data Exfiltration](): A penetration tester encodes sensitive data into DNS queries and sends it to an external server. The test checks if the network's security system detects the unusual amount of DNS traffic or the non-standard nature of the DNS requests.
- Remote Shell: Establishing a remote shell session where commands and outputs are encoded and transferred via DNS queries and responses, allowing control over a compromised system from outside the network.



