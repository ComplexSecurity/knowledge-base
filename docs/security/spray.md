The basics of a password spraying attack involve a threat actor using a single common password against multiple accounts on the same application. This avoids the account lockouts that typically occur when an attacker uses a brute force attack on a single account by trying many passwords. Password spraying is particularly effective against businesses that participate in password sharing.

Password Spraying is a variant of what is known as a [[Brute Force Attack|brute force attack]]. In a traditional brute force attack, the perpetrator attempts to gain unauthorized access to a single account by guessing the password repeatedly in a very short period of time. 

Most organizations have employed countermeasures, commonly a lock-out after three to five attempts. In a Password Spraying attack, the attacker circumvents common countermeasures (e.g., account lock out) by “spraying” the same password across many accounts before trying another password.

Typically used against single sign-on (SSO) and cloud-based applications using federated authentication protocols, this attack allows the malicious actor to compromise the authentication mechanisms. Once in, the attacker moves laterally, capitalizing on internal network vulnerabilities, to gain access to critical applications and sensitive data.

Common tactics, techniques, and procedures (TTPs) involved in this type of attack include:

- Using online research and social engineering tactics to identify target organizations and user accounts
- Using easily guessed passwords (e.g., “Password123”) to execute the password spray attack
- Leveraging compromised accounts to obtain email address lists to attack even more accounts
- Expand laterally within the compromised network and exfiltrate data

