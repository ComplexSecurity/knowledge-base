Patator is a versatile, multi-purpose, and extensible brute-force tool designed for performing penetration testing and security assessments. It is commonly used by security professionals and penetration testers to automate password-cracking and authentication-testing tasks. Patator supports a wide range of protocols, services, and attack methods.

Patator supports a variety of network protocols and services, including [SSH](), [FTP](), [Telnet](), [HTTP](), [RDP](), [VNC](), [IMAP](), [SMB](), and more. It can perform multiple types of attacks, including [dictionary attacks](), [brute-force attacks](), and [hybrid attacks]() (combining dictionary and brute-force methods).

Patator can perform multiple login attempts simultaneously, making it efficient for password-cracking tasks. Users can customize attack parameters, such as usernames, passwords, target hosts, and ports. Patator's modular design allows for the addition of new protocols and services through external modules.

Patator supports both dictionary-based attacks (using wordlists) and pure brute-force attacks. An example may be:

```bash
patator ssh_login host=ssh.example.com user=FILE0 password=FILE1 0=users.txt 1=passwords.txt -x ignore:mesg='Authentication failed.'
```

- `ssh_login`: Specifies the SSH login module.
- `host=ssh.example.com`: Specifies the target SSH server's hostname or IP address.
- `user=FILE0`: Specifies the username parameter and indicates that usernames will be loaded from a file.
- `password=FILE1`: Specifies the password parameter and indicates that passwords will be loaded from a file.
- `0=users.txt`: Specifies the file containing a list of usernames.
- `1=passwords.txt`: Specifies the file containing a list of passwords.
- `-x ignore:mesg='Authentication failed.'`: Instructs Patator to ignore login attempts with the message "Authentication failed."

!!! info
    Patator will attempt to log in to the SSH server by trying each username-password combination from the provided files. If it successfully finds a valid combination, it will report the credentials.