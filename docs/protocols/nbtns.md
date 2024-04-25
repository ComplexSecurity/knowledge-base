NBT-NS (NetBIOS Name Service) is a protocol used in early Windows networking for name resolution, which allows computers on a network to find each other using [[NetBIOS]] names instead of IP addresses. It's part of the [[NetBIOS over TCP-IP (NBT)|NetBIOS-over-TCP/IP]] suite and was commonly used in small networks, particularly before the widespread adoption of [[DNS]] (Domain Name System).

NBT-NS enables computers to register their NetBIOS names on the network and resolve the NetBIOS names of other computers to IP addresses. In a typical setup without a dedicated name server, NBT-NS uses broadcast queries over the local subnet to resolve names. A computer needing to resolve a NetBIOS name sends a broadcast request, and the computer with that name responds with its IP address.

In larger networks, NBT-NS can work with a [[WINS (Windows Internet Name Service)]] server, which acts like a DNS server for NetBIOS names, reducing broadcast traffic and enabling name resolution across different subnets.

NBT-NS was primarily used in small office/home office (SOHO) networks and in legacy corporate networks for local area network (LAN) communications. It played a significant role in facilitating file and printer sharing in early Windows networks.

NBT-NS is susceptible to various security vulnerabilities, including spoofing and [[Man-in-the-Middle (MitM) attack|man-in-the-middle attacks]]. Attackers can exploit NBT-NS to redirect network traffic or impersonate other computers. 

With the rise of DNS and [[Active Directory]], NBT-NS has become largely obsolete in modern network environments. It's generally recommended to disable NetBIOS over TCP/IP in network settings to reduce the attack surface. Despite being outdated, NBT-NS might still be found in some legacy systems or specific network configurations for backward compatibility.
