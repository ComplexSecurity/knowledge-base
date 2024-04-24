Broken authentication is typically caused by poorly implemented authentication and session management functions. Broken authentication attacks aim to take over one or more accounts giving the attacker the same privileges as the attacked user. 

Authentication is “broken” when attackers are able to compromise passwords, keys or session tokens, user account information, and other details to assume user identities.

Due to poor design and implementation of identity and access controls, the prevalence of broken authentication is widespread. Common risk factors include:

- Predictable login credentials
- User authentication credentials that are not protected when stored
- Session IDs exposed in the URL (e.g., URL rewriting)
- Session IDs vulnerable to session fixation attacks
- Session value that does not time out or get invalidated after logout
- Session IDs that are not rotated after successful login
- Passwords, session IDs, and other credentials sent over unencrypted connections

Broken Authentication attackers have only to gain access to a couple of accounts to compromise an entire system by using tools such as automated password tools and dictionary attacks.

Authentication refers to the process of verifying the identity of users, typically through usernames and passwords, while session management involves maintaining and controlling the user's session after authentication.

When these mechanisms are compromised or misconfigured, attackers can exploit the vulnerabilities to gain unauthorized access to user accounts, impersonate other users, or hijack sessions. This can lead to severe security breaches and expose sensitive user information.
