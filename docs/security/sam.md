The Windows Security Account Manager (SAM) is a database file in Windows operating systems that stores user credentials. SAM is used by Windows to manage user accounts and security descriptors, which control access to different resources within the system. The SAM file is a crucial component of the Windows security subsystem.

The SAM file is typically located in the `%SystemRoot%\system32\config` directory. The actual file is `%SystemRoot%\system32\config\SAM`, and it is locked by the system when Windows is running, making it inaccessible to regular users and processes.

SAM contains details about all user accounts on the system, including usernames, password hashes, and other security-related information. Passwords are not stored in plaintext but as hashed values. During the login process, Windows uses the SAM to verify user credentials. When a user enters a password, it is hashed and compared with the stored hash in the SAM.

The SAM file is a target for attackers because it holds hashed passwords. Tools like [Mimikatz]() can extract these hashes, which can then be cracked or used in [pass-the-hash attacks]() to gain unauthorized access. To protect the SAM, Windows restricts its access. Additionally, Windows stores the file in a way that's not easily readable when the system is offline (e.g., booting from an external OS).

Administrators should protect access to SAM and maintain backups. However, they must ensure that these backups are secure, as they contain sensitive data.

In penetration testing, the SAM file is often targeted to extract user credentials. This is typically done by booting the system with an alternative OS or using tools that can read locked files. The extracted hashes can be cracked or used for [Lateral Movement|lateral movement]() within a network.

The SAM file contains information about user accounts on the system. This includes:

- Usernames
- User IDs
- Password hashes
- Group memberships
- Other security-related user account settings

An example representation of the kind of information contained within the SAM file (in a human-readable format) might look like this:

```yaml
Username: JohnDoe
UserID: 1001
Password Hash: 5F4DCC3B5AA765D61D8327DEB882CF99
Group Memberships: Users, Administrators
```

