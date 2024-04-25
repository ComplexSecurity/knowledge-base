Hydra, also known as THC-Hydra, is a popular and powerful password-cracking tool that is used for performing online and offline attacks to guess passwords or perform [[Brute Force Attack|brute-force attacks]] against a variety of network services and protocols. It is a command-line tool often utilized by security professionals and penetration testers to test the strength of authentication mechanisms and identify weak or easily guessable passwords.

Hydra supports a wide range of network protocols and services, including [[Secure Shell|SSH]], [[File Transfer Protocol|FTP]], [[Telnet]], [[HTTP Protocol|HTTP]], [[Remote Desktop Protocol|RDP]], [[Server Message Block|SMB]], [[Simple Network Management Protocol|SNMP]], [[MySQL|MySQL (KB)]], and many others. Users can customize attack parameters, including usernames, passwords, target hosts, ports, and various attack modes.

Hydra is highly parallelized, allowing it to make multiple connection attempts simultaneously, making it efficient for large-scale password-cracking tasks. Hydra supports both [[Dictionary Attacks|dictionary-based attacks]] (using wordlists) and pure brute-force attacks (trying every possible combination).

An example may be:

```bash
hydra -l username -P password-file.txt ssh://target-host
```

- `-l username`: Specifies the target username.
- `-P password-file.txt`: Specifies a file containing a list of passwords to try.
- `ssh://target-host`: Specifies the target SSH server's hostname or IP address.

!!! info
    Hydra will attempt to log in to the SSH server on the target host by trying each password from the provided file (`password-file.txt`). If it successfully finds a valid password, it will report the credentials.

