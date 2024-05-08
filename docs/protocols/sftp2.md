SSH File Transfer Protocol (SFTP), also known as Secure FTP, is a network protocol used for secure file transfer over a [secure shell](../protocols/ssh.md) (SSH) data stream. SFTP is not to be confused with [FTPS (FTP Secure)](../protocols/ftps.md), which is an extension of FTP adding support for [SSL](../cryptography/ssl.md)/[TLS](../cryptography/tls.md). 

SFTP is part of the SSH protocol suite and provides a secure method for file access, file transfer, and file management over a reliable data stream.

SFTP encrypts both the commands and data, providing robust security against eavesdropping, connection hijacking, and other network attacks. Unlike FTP, which uses separate control and data connections, SFTP uses a single connection for both commands and data transfer. This simplifies firewall configurations and reduces the chances of data being intercepted.

SFTP supports multiple forms of authentication, including password-based and public key authentication. The connection is established over the SSH protocol, ensuring secure authentication.

Besides file transfer, SFTP allows for a range of file management operations like creating and deleting directories and files, resuming interrupted transfers, and listing directory contents.

SFTP operates over an SSH session, typically on [TCP](../networking/tcp.md) port 22. It starts by establishing an SSH connection between the client and server. All SFTP packets are sent encrypted over this established SSH session. 

The client authenticates to the SFTP server using SSH authentication methods. This can be password authentication, public key authentication, or Kerberos authentication. Once authenticated, the client can execute a range of file operations through the SFTP session. The commands and data are all encrypted.

The differences between SFTP and FTPS are:

- **SFTP (SSH File Transfer Protocol)**: A secure file transfer protocol that runs over an SSH session. It's not related to FTP and uses a different protocol entirely.
- **FTPS (FTP Secure)**: An extension of the FTP protocol, adding support for SSL/TLS to encrypt the FTP traffic.


