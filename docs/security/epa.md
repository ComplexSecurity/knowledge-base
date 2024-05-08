Extended Protection for Authentication (EPA) is a security feature designed to enhance protection against [Man-in-the-Middle (MitM) attack|man-in-the-middle (MITM) attacks]() during the authentication process in network communications. It primarily strengthens the security of authentication protocols like [NTLM]() and [Kerberos Authentication|Kerberos]() in Windows environments.

EPA employs [Channel Binding Tokens (CBTs)]() to bind the authentication process to a specific secure channel (like [TLS]()). This ensures that the authentication process is not being relayed or redirected by an attacker to another channel or session, a technique often used in MITM attacks.

EPA is effective in preventing attacks like NTLM relay attacks, where an attacker intercepts and forwards authentication credentials to access network resources illegitimately. It enables servers to confirm that the authentication requests they receive are coming directly from the client and are associated with the current secure session.

EPA is often used in conjunction with services like [Microsoft IIS|Internet Information Services (IIS)]() to secure web applications, ensuring that the authentication process is tightly integrated with the TLS session. In scenarios where protocols like NTLM and Kerberos are used, EPA provides an additional layer of security against credential theft and replay attacks.

Configuring EPA on a web server to require that all [Basic HTTP Authentication|HTTP authentication]() requests include a CBT, thereby mitigating the risk of NTLM relay attacks. In [Active Directory]() environments, EPA can be configured for services like [AD FS (Active Directory Federation Services)]() to ensure secure authentication processes.
