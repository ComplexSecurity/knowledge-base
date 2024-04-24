Bearer token authentication is a method of securing access to resources on the web, often used in the context of [[HTTP Protocol|HTTP]] (Hypertext Transfer Protocol) authentication. It is a simple and widely adopted approach for authenticating and authorizing users or clients to access protected resources in web applications and [[APIs]].

In bearer token authentication, a "bearer token" is a piece of cryptographic information (often a long string of characters) that serves as proof of the authenticated user or client's identity. This token is generated and issued by an identity provider or authentication server when a user logs in or a client application obtains access to a protected resource.

Instead of sending credentials (e.g., username and password) with every HTTP request, the client presents the bearer token in the request headers to access protected resources. The token is included in the `Authorization` header of the HTTP request using the "Bearer" scheme. For example:

```makefile
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...
```

Bearer token authentication is stateless, meaning that the server does not need to store or maintain session information. Each request sent by the client contains all the necessary authentication information in the bearer token itself. This simplicity makes bearer tokens suitable for scaling and distributed systems.

The server receiving the bearer token validates it to ensure its authenticity and check whether the token is still valid. The validation process may involve verifying the token's signature, checking the expiration time, and confirming that the token has not been revoked.

Bearer tokens can carry additional information, such as user roles, permissions, or scopes, which can be used by the server to determine the level of access or actions the bearer of the token is allowed to perform.

Bearer token authentication is commonly used in various scenarios, including:

- [[OAuth]] 2.0: Bearer tokens are a fundamental component of OAuth 2.0 for authorizing third-party applications to access user data on behalf of the user.
- API Authentication: Many [[REST APIs|RESTful]] APIs and web services use bearer tokens to secure access to their resources.
- [[Single Sign-On (SSO)]]: In some SSO systems, bearer tokens are used as proof of authentication and authorization for accessing multiple applications.

While bearer tokens are convenient and widely used, it's essential to secure them properly. They can be vulnerable if not handled securely. Best practices include using [[HTTPS Protocol|HTTPS]] for communication, protecting tokens from disclosure, and implementing token revocation mechanisms.

