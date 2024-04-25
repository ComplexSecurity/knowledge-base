A pass-the-hash (PtH) attack is a technique used by attackers to authenticate to a remote server or service using a hashed version of a user's password, rather than requiring the actual plaintext password. This type of attack exploits the way Windows and other systems handle and store password hashes.

First, an attacker obtains the hashed version of a user's password. This can be done through various methods, such as extracting the hashes from a compromised system (often from the [[SAM]] file in Windows) or intercepting the hash over the network.

Instead of cracking the password hash to reveal the plaintext password (which can be time-consuming and difficult), the attacker uses the hash itself to authenticate. Many systems use a challenge-response mechanism for authentication, where the hash plays a crucial role. The attacker essentially responds to the authentication challenge by using the acquired hash.

Consider a scenario where an attacker has gained access to a Windows system and has extracted password hashes from the system, typically from the Security Account Manager (SAM) database or the [[Active Directory]] database.

Using tools like [[Mimikatz]], an attacker extracts the [[NTLM]] hash of a user's password from the compromised system. The attacker then uses this hash to authenticate to another system or service within the network as the user whose hash was stolen. This is often done using tools that allow the specification of an NTLM hash instead of a plaintext password.

If successful, the attacker gains access to the target system or service with the same level of privileges as the user whose hash was used. This can lead to lateral movement within the network, accessing sensitive data, or further compromising network security.

Several tools are commonly used in cybersecurity, particularly in penetration testing and ethical hacking, to perform pass-the-hash (PtH) attacks. These include:

1. Mimikatz: Perhaps the most well-known tool in this category, Mimikatz can extract password hashes from memory, perform pass-the-hash attacks, pass-the-ticket, and more. It's a versatile tool for various types of Windows credentials-related attacks.
2. [[Metasploit Framework]]: Metasploit, a widely used penetration testing framework, includes modules that can perform pass-the-hash attacks. These modules allow testers to use extracted hashes to authenticate to other systems.
3. [[Windows Credential Editor (WCE)]]: WCE is a tool similar to Mimikatz that can be used for extracting NTLM password hashes and performing pass-the-hash attacks.
4. [[Hashcat]]: While primarily known as a [[password cracking]] tool, Hashcat can be used in certain scenarios to perform pass-the-hash attacks, especially where the hash mode supports it.
5. [[CrackMapExec]]: This is a post-exploitation tool that automates the assessment of large Active Directory networks. It includes functionality for pass-the-hash attacks.
6. [[PTH-Toolkit]]: A collection of scripts that enable some tools to use NTLM hashes for authentication, effectively enabling pass-the-hash capabilities in those tools.
7. [[Empire]]: A [[Pass-the-Hash Attacks]] and [[Python]] post-exploitation agent, Empire has capabilities for performing pass-the-hash attacks among its many features for exploiting Windows systems.