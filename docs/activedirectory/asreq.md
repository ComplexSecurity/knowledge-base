The Authentication Request (AS-REQ) is a critical part of the initial authentication phase in the [Kerberos authentication](../activedirectory/kerb.md) protocol. It is the request sent by a client (usually a user or a service) to the Kerberos [Authentication Service (AS)](../activedirectory/as.md) when seeking authentication within a network environment.

The process begins with the client generating an AS-REQ. This request is sent to the AS to obtain a [Ticket Granting Ticket (TGT)](../activedirectory/tgt.md). The AS-REQ includes the client's principal name (essentially their identity in the Kerberos realm, like a username). 

!!! info
    To protect against replay attacks, the AS-REQ typically includes a timestamp, which is encrypted with the client's password or a derived key. This encryption confirms that the request is from the legitimate user and has not been tampered with.

The AS-REQ also indicates the service for which authentication is being requested. Initially, this is usually the [Ticket Granting Service (TGS)](../activedirectory/tgs.md). 

The AS-REQ is the first step in the Kerberos authentication process. It initiates the sequence of securing a TGT, which is then used for obtaining service tickets for various services within the network. Upon receiving the AS-REQ, the AS verifies the encrypted timestamp using the password (or key) stored in its database for the principal. This confirms the identity of the user.

If the verification is successful, the AS responds with an [Authentication Service Response (AS-REP)](../activedirectory/asresponse.md), which includes the TGT and a session key for further communication.

The use of an encrypted timestamp in the AS-REQ helps mitigate replay attacks, where an attacker might try to reuse a valid request to gain unauthorized access. The encryption ensures the confidentiality and integrity of the authentication request, essential in a secure network environment.
