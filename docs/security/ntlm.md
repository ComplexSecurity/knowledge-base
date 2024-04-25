NTLM, which stands for "NT LAN Manager," is a suite of authentication and security protocols developed by Microsoft. NTLM is primarily used for network authentication in Windows environments and is a predecessor to more modern authentication mechanisms like [[Kerberos Authentication|Kerberos]] and NTLMv2. It is designed to provide secure authentication for users and computers within a Windows domain.

NTLM is used to authenticate users and computers when they attempt to access resources on a Windows-based network. It verifies the identity of the user or computer by checking their credentials (e.g., username and password). NTLM has several versions, including NTLMv1 and NTLMv2. NTLMv2 is more secure and recommended over NTLMv1 due to vulnerabilities in the latter.

NTLM authentication relies on a challenge-response mechanism. When a user or computer attempts to log in, the server (or authentication authority) sends a random challenge to the client. The client then encrypts the challenge using the user's password and sends the encrypted response back to the server for verification.

NTLM is commonly used in Windows domains for authenticating users and computers against a domain controller. This ensures that users have valid domain credentials before gaining access to domain resources.

NTLM supports [[Single Sign-On (SSO)]] in Windows environments. Once a user logs in to a Windows computer, their credentials can be cached, allowing them to access other network resources without re-entering their credentials.

NTLM has some limitations and security concerns, particularly with NTLMv1. It is vulnerable to certain types of attacks, including pass-the-hash attacks, and it does not support mutual authentication, making it less secure than more modern authentication protocols like Kerberos.

In Windows domains, NTLM has largely been replaced by the Kerberos authentication protocol, which offers improved security and support for mutual authentication. However, NTLM may still be used in legacy environments or when Kerberos is not feasible. NTLM is still supported in Windows environments for backward compatibility with legacy systems and applications that rely on it.