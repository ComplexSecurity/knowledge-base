Digest authentication is one of the [[HTTP Protocol|HTTP]] authentication methods used to secure web applications and services. It is designed to address some of the security weaknesses of the [[Basic HTTP Authentication|Basic Authentication]] method by providing a more secure way for clients and servers to authenticate each other.

Digest authentication operates on a challenge-response mechanism, similar to Basic Authentication. However, it improves security by not transmitting plaintext passwords over the network.

Instead of sending passwords directly, Digest authentication requires the client to send a hashed version of the password. This hashing is done using a one-way cryptographic hash function, such as [[MD5]] or [[SHA-256]]. The server also stores hashed versions of user passwords.

The server sends a unique "nonce" value (a random number or string) in the authentication challenge. The nonce is used to prevent replay attacks. The client includes this nonce in the hashed response. The server specifies a "realm" in the challenge, which is a description of the protected area or security domain. The client may display this realm to the user, allowing the user to provide the appropriate credentials.

Digest authentication can support various "quality of protection" options, such as "auth" (authentication) and "auth-int" (authentication with message integrity). The QOP value is included in the authentication parameters.

To create the response, the client hashes several pieces of information, including the username, password, nonce, realm, request method, URI, and other parameters. This hashed value is sent to the server. Digest authentication provides a higher level of security compared to Basic Authentication because it does not transmit plaintext passwords over the network. However, it is not considered as secure as modern authentication mechanisms like [[Knowledge Base/OAuth]] 2.0.

The client includes the `Authorization` header in the HTTP request with the "Digest" scheme and the calculated response. For example:

```sql
Authorization: Digest username="alice", realm="Example", nonce="dcd98b7102dd2f0e8b11d0f600bfb0c093", uri="/resource", response="f3a2556be9021ac2db4e06d562396fa8", qop=auth, nc=00000001, cnonce="0a4f113b", opaque="5ccc069c403ebaf9f0171e9517f40e41"
```

Upon receiving the authentication information, the server calculates the expected response based on the stored information and compares it to the received response. If they match, the client is authenticated. The client includes a nonce count (NC) value in the authentication parameters to prevent replay attacks. The server tracks the NC value to ensure that each request is unique.
