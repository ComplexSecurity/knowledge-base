TACACS+ (Terminal Access Controller Access-Control System Plus) is an advanced protocol used for remote authentication and access control to network devices such as routers, switches, and [[Firewall|firewalls]]. It is an enhancement of the original TACACS protocol and provides more flexibility and security.

Unlike its predecessors, TACACS+ separates authentication, authorization, and accounting services. This separation allows for more granular control and flexibility in managing network access.

TACACS+ authenticates users trying to access a network device. It supports various authentication methods, including password, [[PAP (Password Authentication Protocol)]], [[CHAP (Challenge Handshake Authentication Protocol)]], and more.

After authentication, TACACS+ manages what commands or services the user is authorized to perform or use on the network device. It keeps detailed logs of user activities, such as what commands were executed, providing an audit trail that can be crucial for security and compliance.

One of the significant advantages of TACACS+ over older protocols like [[RADIUS]] is that it encrypts the entire body of the request packets, providing more security for sensitive data like user passwords.

TACACS+ uses TCP ([[Transmission Control Protocol]]) for reliable transport. By default, it operates on port 49. TACACS+ allows network administrators to centrally manage and control user access to network devices, simplifying the administration of network security.

TACACS+ is extensible and supports vendor-specific options, allowing customization for different network environments and devices. While it is an open standard, TACACS+ has been primarily used in Cisco environments, as it was developed by Cisco Systems.

While TACACS+ and RADIUS are both used for similar purposes, TACACS+ offers more granular control at the command level and encrypts the entire packet payload, not just the password. However, RADIUS is more commonly used and supports a wider range of network devices beyond Cisco.


