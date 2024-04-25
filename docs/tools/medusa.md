Medusa is a command-line, cross-platform, and modular network login brute-forcing tool. It is designed for performing [[Brute Force Attack|brute-force attacks]] against various network protocols and services to guess usernames and passwords. Medusa supports a wide range of authentication protocols, making it a versatile tool for security assessments and penetration testing.

Medusa supports a variety of network protocols and services, including [[Secure Shell|SSH]], [[File Transfer Protocol|FTP]], [[HTTP Protocol|HTTP]], [[Remote Desktop Protocol|RDP]], [[Server Message Block|SMB]], [[Post Office Protocol|POP3]], [[Internet Message Access Protocol|IMAP]], [[MySQL|MySQL (KB)]], and more. It can perform multiple login attempts simultaneously, making it efficient for password-cracking tasks.

Medusa's modular design allows for the addition of new protocols and services through external modules. Users can customize attack parameters, such as usernames, passwords, and attack timeouts.

Medusa supports both [[Dictionary Attacks|dictionary-based attacks]] (using wordlists) and pure [[Brute Force Attack|brute-force attacks]].

An example may be:

```bash
medusa -h target-ftp-server -U users.txt -P passwords.txt -M ftp
```

- `-h target-ftp-server`: Specifies the target FTP server's hostname or IP address.
- `-U users.txt`: Specifies a file containing a list of usernames to try.
- `-P passwords.txt`: Specifies a file containing a list of passwords to try.
- `-M ftp`: Specifies the FTP module for Medusa to use.

!!! info
    Medusa will attempt to log in to the FTP server by trying each username-password combination from the provided files. If it successfully finds a valid combination, it will report the credentials.

