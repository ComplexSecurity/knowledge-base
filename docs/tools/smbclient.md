Impacket's `smbclient` is a tool within the [[Impacket]] suite that acts similarly to Microsoft's command-line SMB client. It's used for interacting with [[Server Message Block|SMB]]/[[CIFS]] shares on Windows and other systems that support the SMB/CIFS protocol. With Impacket's `smbclient`, you can list shares, upload, download, delete files, and create or remove directories on the SMB server.

You can enumerate shares available on the SMB server. You can also upload, download, delete files, and create or delete directories on the SMB server. Some versions allow for executing commands on the server. Finally, it supports [[NTLM]] authentication, making it useful for testing and exploiting Windows networks.

A basic example of how to use Impacket's `smbclient` to list shares on a remote SMB server. This example assumes you have Impacket installed and are running its scripts from the command line:

```bash
python smbclient.py 'DOMAIN/username:password'@<IP_ADDRESS>
```

After running this command, you will be presented with an interactive SMB shell where you can run commands like `ls`, `put`, `get`, `mkdir`, `rmdir`, etc., to interact with the server's file system.

For instance, to list files in a share named `SHARENAME`, you would use:

```bash
smb> use SHARENAME
smb> ls
```

