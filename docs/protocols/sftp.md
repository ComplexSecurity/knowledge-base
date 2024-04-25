Secure File Transfer Protocol (SFTP), sometimes referred to as SSH File Transfer Protocol, is a network protocol used for secure file transfer over a [[secure shell]] (SSH) data stream. SFTP is often confused with [[FTPS (File Transfer Protocol Secure)]], but they are distinct protocols.

SFTP provides a secure method for transferring files by using SSH for data transmission, ensuring that both the data and commands are encrypted. SFTP requires authentication of the client to the server, typically through username and password, SSH keys, or both.

The use of SSH ensures that data is not only encrypted during transfer but also protected from unauthorized access or eavesdropping. Unlike [[SCP (Secure Copy)]], SFTP allows for a range of operations on remote files, such as browsing and managing directories, in addition to transferring files. SFTP is widely supported across different operating systems, making it a versatile choice for file transfer needs in diverse environments.

In comparison to other protocols:

- [[File Transfer Protocol|FTP]] is an older protocol that doesn't inherently support encryption, making it less secure than SFTP.
- FTPS is an extension of FTP with [[TLS]] encryption. While it also provides secure file transfer, it differs from SFTP in its use of separate control and data connections and its reliance on [[SSL-TLS|SSL/TLS]] as opposed to SSH.
- SCP is another SSH-based protocol but is primarily used for transferring files. SFTP offers more functionality, such as the ability to list and manage files on the server.

