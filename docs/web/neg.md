Negotiate authentication is one of the [[HTTP Protocol|HTTP]] authentication mechanisms used to secure web applications and services. It is primarily associated with Microsoft Windows environments and is often referred to as "**Negotiate**" or "**SPNEGO**" ([[Simple and Protected GSSAPI Negotiation Mechanism]]). Negotiate authentication is designed to provide a mechanism for [[Single Sign-On (SSO)]] and interoperability with various authentication protocols, including [[NTLM]] and [[Kerberos Authentication|Kerberos]].

The term "Negotiate" indicates that the client and server negotiate the authentication protocol to use during the authentication process. The negotiation typically happens as follows:

- The client sends an initial HTTP request to the server without any authentication information.
- The server responds with a `WWW-Authenticate` header field that includes "Negotiate" as one of the supported authentication methods.
- The client selects an appropriate authentication protocol (e.g., Kerberos or NTLM) based on its capabilities and the server's preferences.
- The client sends another HTTP request, this time including the selected authentication protocol (e.g., "Negotiate" followed by the authentication token).

Negotiate authentication allows clients to use either the Kerberos protocol (if available) or the NTLM protocol for authentication. It prioritizes the use of Kerberos when possible, as it is considered more secure than NTLM.

Negotiate authentication enables SSO within a Windows domain or Kerberos realm. Once a user logs in to their Windows computer, they can access web resources without having to re-enter their credentials.

In the Negotiate authentication process, the client and server exchange security tokens. These tokens are used to prove the identity of the client. The tokens can be Kerberos tickets or NTLM challenge-response tokens, depending on the chosen authentication protocol.

Negotiate authentication relies on the [[Generic Security Services Application Programming Interface (GSSAPI)]], which provides a framework for secure communication. GSSAPI enables the negotiation of security mechanisms and the exchange of security tokens.

Negotiate authentication is primarily associated with Microsoft technologies, but it can also be used in non-Microsoft environments, provided that the server and client support the Negotiate mechanism and the chosen authentication protocol. If Kerberos authentication is not available or fails, the client may fall back to using NTLM authentication for compatibility.

