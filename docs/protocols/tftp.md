TFTP, or Trivial File Transfer Protocol, is a simple high-level protocol for transferring data servers use to boot diskless workstations, X-terminals, and routers by using [[User Datagram Protocol|UDP]].

Although it may sound similar, TFTP works differently than [[File Transfer Protocol|FTP]] (File Transfer Protocol) and [[HTTP Protocol]]. Although TFTP is also based in FTP technology, TFTP is an entirely different protocol. Among the differences is that TFTP’s transport protocol uses UDP which is not secure while FTP uses [[Transmission Control Protocol]] (TCP) to secure information.

TFTP was primarily designed to read or write files by using a remote server. However, TFTP is a multi-purpose protocol that can be leveraged for an array of different tasks. 

TFTP does not need to authenticate a user. As a user, you only need to know the file’s name you’re trying to download, and you can send a command to request that specific file. TFTP is also slower in its transferring process. This is due to the fact that the TFTP server needs to divide data into pieces when transferring it to the TFTP client.