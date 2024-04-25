EternalBlue is a cyber attack exploit developed by the U.S. National Security Agency (NSA). It became widely known in April 2017 when it was leaked by the hacker group known as The Shadow Brokers. EternalBlue exploits a vulnerability in Microsoft's implementation of the [[Server Message Block]] (SMB) protocol.

EternalBlue targets a vulnerability in [[SMB 1]], a network file sharing protocol used by Windows. The specific vulnerability is identified as CVE-2017-0144. It allows for [[remote code execution]], meaning an attacker could send specially crafted packets to a vulnerable Windows machine, allowing them to execute arbitrary code.

The attacker scans for and identifies machines running vulnerable versions of Windows SMBv1. The attacker crafts and sends specially designed packets to the SMB port (445) of the target machine. These packets exploit the vulnerability to allow remote code execution. Once the exploit is successful, the attacker can execute code on the affected machine. This often involves installing a backdoor for persistent access or deploying malware.

A well-known example of EternalBlue's exploitation is the WannaCry ransomware attack in May 2017. In this attack:

- Attackers used EternalBlue to remotely access vulnerable Windows systems on a global scale.
- After gaining access, the WannaCry ransomware was deployed, which encrypted files on the infected systems.
- Victims were asked to pay a ransom in Bitcoin to get their files decrypted.
