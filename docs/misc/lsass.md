LSASS (Local Security Authority Subsystem Service) is a critical process in Microsoft Windows operating systems that is responsible for enforcing the security policy on the system. It handles user logins, authentication, and creates security tokens. LSASS also writes to the Windows Security Log.

LSASS verifies the validity of user logins to a PC or server. When a user logs into a Windows computer, LSASS generates the user's access token, which defines their privileges. LSASS is involved in changing passwords for user accounts. It enforces various security policies and acts as a gatekeeper for accessing sensitive information.

LSASS is a target for attackers due to its critical role in handling authentication and storing credentials:

1. **Credential Dumping**: Tools like [[Mimikatz]] exploit LSASS to extract passwords, [[NTLM]] hashes, and Kerberos tickets. This information can then be used for [[lateral movement]], [[privilege escalation]], or further penetration into the network.
2. [[Pass-the-Hash Attacks|Pass-the-Hash (PtH) Attacks]]: Attackers can use NTLM hashes extracted from LSASS for PtH attacks, allowing them to authenticate to other systems without needing the plaintext password.
3. **Memory Dumping**: Attackers may dump the LSASS process memory to extract sensitive information. This can be done by injecting code into the LSASS process or using debugging tools.
4. **Persistence and Evasion**: Malware may inject itself into the LSASS process to hide its presence, as terminating LSASS can cause the system to crash, thus avoiding detection.

