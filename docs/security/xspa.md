A Cross-Site Port Attack (XSPA) is a type of network security vulnerability that allows an attacker to exploit the behavior of a web application to conduct port scanning of internal hosts or other external hosts from the victim’s browser. Essentially, it leverages the victim's system to scan and map network ports, which can reveal information about active services and vulnerabilities on those hosts.

The attacker identifies a web application that can be used as a proxy for port scanning. This application might be vulnerable due to improper security checks or certain functionalities (like [HTTP Protocol|HTTP]() requests, [WebSockets|WebSocket]() connections, or others) that can be manipulated.

The attacker then crafts requests from this application to target internal or external systems. These requests attempt to establish connections to various ports on the specified hosts. Based on the web application’s responses (or lack thereof) to these requests, the attacker can infer which ports are open. For example, a specific error message or a timeout might indicate whether a port is open or closed.

By systematically scanning different ports, the attacker can map out the network infrastructure, identifying available services or potentially vulnerable systems.

Some examples of XSPA include:

- **Internal Network Scanning**: An attacker uses a vulnerable web application within a corporate network to scan for open ports on internal servers, potentially exposing sensitive services like database management systems, email servers, or administrative interfaces.
- **External Host Scanning**: Using a publicly accessible web application to scan ports on external systems, which could be used for gathering intelligence before an attack.
