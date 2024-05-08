SCP (Secure Copy Protocol) is a network protocol that supports file transfers between hosts on a network. It uses SSH ([Secure Shell](../protocols/ssh.md)) for data transfer and provides the same authentication and security as SSH. Unlike the standard file copy commands, SCP ensures that both the file and the communication channel are secure.

SCP uses SSH for data transfer, ensuring that the entire transmission is encrypted and secure from eavesdropping. It leverages SSH's authentication, requiring valid credentials for access to both the source and destination systems. SCP is typically used via a command-line interface, allowing for easy integration with scripts and other automated processes.

SCP is commonly used for:

- **Securely Copying Files Between Systems**: Transferring files securely between servers in a network.
- **Backup and Archiving**: Moving data to a remote server for backup purposes.
- **Administrative Tasks**: Performing file operations securely in scripts and automation processes.

An example may be copying a file from a local to a remote system:

```bash
scp /path/to/local/file.txt username@remotehost:/path/to/remote/directory/
```

!!! info
    This command will copy `file.txt` from the local machine to the specified directory on the remote host.

Or copying a file from a remote system to a local system:

```bash
scp username@remotehost:/path/to/remote/file.txt /path/to/local/directory/
```

!!! info
    This command will copy file.txt from the remote host to the specified directory on the local machine.

You can also copy a directory recursively:

```bash
scp -r /path/to/local/directory username@remotehost:/path/to/remote/directory/
```

!!! info
    The `-r` flag is used to recursively copy an entire directory.

Finally, you can use an SSH key alongside it:

```bash
scp -i /path/to/private/key file.txt username@remotehost:/path/to/remote/directory/
```

!!! info
    The `-i` option allows you to specify an SSH private key to be used for authentication.

SCP ensures that files are encrypted during transfer, providing a high level of security, especially when transferring sensitive data over the internet or unsecured networks. SCP may not be the fastest file transfer method due to the encryption/decryption overhead. For larger transfers, other protocols like [rsync](../tools/rsync.md) or [SFTP](../protocols/sftp.md) might be more efficient.





