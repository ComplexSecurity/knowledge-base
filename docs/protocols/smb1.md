SMB 1, the first version of the [[Server Message Block]] (SMB) protocol, is a network file sharing protocol originally designed to allow computers to read and write files to a remote host over a network. 

SMB 1 was primarily used for sharing files and printers across Windows networks. It supported network browsing, which allowed users to see other computers and shared resources on the network. SMB 1 included a basic level of authentication to control access to shared resources. 

It introduced a form of file locking that allowed for performance improvements and caching optimizations. Over the years, SMB 1 was extended by Microsoft to add additional features, although the core protocol remained limited in terms of security and performance.

SMB 1 is considered insecure by modern standards. It lacks encryption and is susceptible to several types of attacks, including [[Man-in-the-Middle (MitM) attack|man-in-the-middle attacks]]. SMB 1 was infamously exploited by the WannaCry ransomware attack and other malicious software, leading to widespread calls to disable or decommission the protocol.

Compared to its successors ([[SMB 2]] and [[SMB 3]]), SMB 1 is less efficient in terms of speed and resource utilization, particularly over [[Wide Area Network (WAN)|wide area networks]] (WANs). Due to its security and performance limitations, SMB 1 has largely been replaced by SMB 2 and SMB 3 in modern networks. These newer versions provide significant improvements, including enhanced security features (like encryption), better performance, and additional functionalities.

!!! danger
    Given its vulnerabilities, it's a security best practice to disable SMB 1 in networks where it's not strictly required for legacy compatibility. 

