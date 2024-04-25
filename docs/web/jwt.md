JSON Web Token is an open industry standard used to share information between two entities, usually a client (like your app’s frontend) and a server (your app’s backend).

They contain [[JavaScript Object Notation|JSON]] objects which have the information that needs to be shared. Each JWT is also signed using cryptography (hashing) to ensure that the JSON contents (also known as JWT claims) cannot be altered by the client or a malicious party.

JSON web tokens (JWTs) are a standardized format for sending cryptographically signed JSON data between systems. They can theoretically contain any kind of data, but are most commonly used to send information ("claims") about users as part of authentication, session handling, and access control mechanisms.

Unlike with classic session tokens, all of the data that a server needs is stored client-side within the JWT itself. This makes JWTs a popular choice for highly distributed websites where users need to interact seamlessly with multiple back-end servers.

A JWT consists of 3 parts: a header, a payload, and a signature. These are each separated by a dot, as shown in the following example:

```JSON
eyJraWQiOiI5MTM2ZGRiMy1jYjBhLTRhMTktYTA3ZS1lYWRmNWE0NGM4YjUiLCJhbGciOiJSUzI1NiJ9.eyJpc3MiOiJwb3J0c3dpZ2dlciIsImV4cCI6MTY0ODAzNzE2NCwibmFtZSI6IkNhcmxvcyBNb250b3lhIiwic3ViIjoiY2FybG9zIiwicm9sZSI6ImJsb2dfYXV0aG9yIiwiZW1haWwiOiJjYXJsb3NAY2FybG9zLW1vbnRveWEubmV0IiwiaWF0IjoxNTE2MjM5MDIyfQ.SYZBPIBg2CRjXAJ8vCER0LA_ENjII1JakvNQoP-Hw6GG1zfl4JyngsZReIfqRvIAEi5L4HV0q7_9qGhQZvy9ZdxEJbwTxRs_6Lb-fZTDpW6lKYNdMyjw45_alSCZ1fypsMWz_2mTpQzil0lOtps5Ei_z7mM7M8gCwe_AGpI53JxduQOaB5HkT5gVrv9cKu9CsW5MS6ZbqYXpGyOG5ehoxqm8DL5tFYaW3lB50ELxi0KsuTKEbD0t5BCl0aCR2MBJWAbN-xeLwEenaqBiwPVvKixYleeDQiBEIylFdNNIMviKRgXiYuAvMziVPbwSgkZVHeEdF5MQP1Oe2Spac-6IfA
```

Header and payload parts of a JWT are just base64 encoded JSON objects. The header contains metadata about the token itself, while the payload contains the actual "claims" about the user. For example, you can decode the payload from the token above to reveal the following claims:

```JSON
{
    "iss": "portswigger",
    "exp": 1648037164,
    "name": "Carlos Montoya",
    "sub": "carlos",
    "role": "blog_author",
    "email": "carlos@carlos-montoya.net",
    "iat": 1516239022
}
```

The server that issues the token typically generates the signature by hashing the header and payload. In some cases, they also encrypt the resulting hash. Either way, this process involves a secret signing key. This mechanism provides a way for servers to verify that none of the data within the token has been tampered with since it was issued:

As the signature is directly derived from the rest of the token, changing a single byte of the header or payload results in a mismatched signature.

Without knowing the server's secret signing key, it shouldn't be possible to generate the correct signature for a given header or payload.



