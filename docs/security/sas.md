Security Associations (SAs) are fundamental components of the [[IPsec]] (Internet Protocol Security) framework, which is used to secure IP communications by authenticating and encrypting each IP packet in a communication session. 

An SA is a logical connection between two entities that describes how they will use security services to communicate securely.

An SA is a set of policies and keys that define how two network entities will secure communication. It includes all the information required to execute various security services, such as the encryption algorithm, the encryption key, and the authentication method.

Each SA is unidirectional. In IPsec, a one-way communication channel requires two SAs, one for inbound traffic and another for outbound traffic. A typical SA contains parameters such as:

- The encryption algorithm (e.g., [[Advanced Encryption Standard (AES)|AES]], [[Triple DES (3DES)|3DES]]).
- The encryption key and its lifetime.
- The authentication algorithm (e.g., HMAC-SHA1).
- The IP addresses of the source and destination.
- A unique identifier called the Security Parameter Index (SPI).

SAs can be established manually or dynamically. Dynamic establishment of SAs is usually done through the [[Internet Key Exchange (IKE)]] protocol, which is part of the IPsec suite. In IPsec, SAs can apply to either Tunnel Mode or Transport Mode, determining how the data will be encrypted and/or authenticated.

Each SA has a lifetime after which it expires and needs to be renewed. This can be based on time or the amount of data transmitted. 

Devices implementing IPsec maintain a database of SAs, known as the Security Association Database (SAD). This database is used to store and retrieve all relevant information about each SA.

SAs play a crucial role in [[Virtual Private Network|Virtual Private Networks]] (VPNs) where IPsec is used. They ensure that each VPN tunnel has the appropriate security parameters to protect the data being transmitted.

The SPD is used in conjunction with the SAD. While the SAD contains the parameters of the SA, the SPD defines the policies that determine the establishment and maintenance of SAs.

