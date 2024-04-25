The Authorization header is a part of the [[HTTP Protocol|HTTP]] (Hypertext Transfer Protocol) request header used in web communications. It contains the credentials to authenticate a user agent (such as a web browser) with a server, typically after the server has responded with a `401 Unauthorized` status code and the [[WWW-Authenticate]] header.

The Authorization header is used to authenticate a user to a server. It carries credentials in the form of a token which can be a username and password, a bearer token, or other forms of tokens. It helps the server determine whether a client has permission to access a requested resource.

The Authorization header generally has the following format:

```php
Authorization: <type> <credentials>
```

- **\<type>**: This is the authentication method used. Common types include:
    - `Basic`: For [[Basic HTTP Authentication|Basic access authentication]], credentials are constructed by encoding the username and password joined by a colon into a [[base64]] string.
    - `Bearer`: Used with [[OAuth]] 2.0 and [[JSON Web Tokens|JWT (JSON Web Tokens)]], where credentials are a token string.
    - `Digest`: For [[Digest Authentication|Digest access authentication]], offering a more secure approach than Basic authentication.
- **\<credentials>**: The actual credentials or token required by the server for authentication. Its format and content vary depending on the `<type>`.

An example may be:

```php
Authorization: Basic dXNlcm5hbWU6cGFzc3dvcmQ=
```

!!! info
    Here, "dXNlcm5hbWU6cGFzc3dvcmQ=" is a base64-encoded string of "username:password".

A bearer token in OAuth 2.0 may appear to be:

```php
Authorization: Bearer mF_9.B5f-4.1JqM
```

!!! info
    The "mF_9.B5f-4.1JqM" is a token granted by the authorization server.

Since the Authorization header often contains sensitive information, it's crucial to transmit it over secure channels (such as [[HTTPS Protocol|HTTPS]]) to prevent eavesdropping. Tokens or credentials in the Authorization header should be securely stored and managed to prevent unauthorized access.

