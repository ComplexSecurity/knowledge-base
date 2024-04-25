CHAP (Challenge Handshake Authentication Protocol) is an authentication protocol used in networking that provides a more secure method of ensuring the identity of a remote user, or node, trying to connect to a service or resource. It's commonly used in [[Point-to-Point Protocol (PPP)]] connections.

Unlike a basic username and password authentication that occurs only at the time of initial connection, CHAP performs repeated authentication at random intervals during the session. This helps protect against unauthorized access in the middle of a connection.

CHAP works on a challenge-response mechanism. When a client attempts to establish a connection, the server sends a challenge message to the client. The client responds with a value obtained by using a one-way hash function on the challenge, along with the client's password and a shared secret.

The actual password is never sent over the network. Instead, the hash result is transmitted, minimizing the risk of password interception.

The CHAP protocol uses a [[Handshake|three-way handshake]].

- The server sends a challenge to the client.
- The client responds with a value calculated using a hash function.
- The server checks the response by comparing it to its own calculation of the expected hash value. If they match, the server acknowledges the authentication; otherwise, the connection is terminated.

CHAP is frequently used in PPP networks, including many types of broadband Internet connections (like DSL). CHAP provides more security than the [[Password Authentication Protocol (PAP)]], which is another authentication protocol used in PPP connections. PAP transmits passwords in clear text, making them more susceptible to interception.

CHAP can be configured for mutual authentication, where both the server and client authenticate each other. If the initial authentication fails, CHAP allows the server to send a new challenge to the client, and the client can try to authenticate again.

There are variants of CHAP, such as Microsoft CHAP (MS-CHAP) and MS-CHAP v2, which are used in different networking contexts and provide additional features like stronger encryption methods.

In a network using CHAP, both the client and server must be configured with the shared secret for authentication to succeed. This requires careful management of these shared secrets.
