OAuth (Open Authorization) is an open standard for access delegation, commonly used to grant websites or applications access to user information on other websites without giving them the passwords. It provides a process for end-users to authorize third-party access to their server resources without sharing their credentials. 

Designed specifically for use with Hypertext Transfer Protocol ([[HTTP Protocol|HTTP]]), OAuth essentially allows an application to act on behalf of a user.

There are two major versions – OAuth 1.0 and OAuth 2.0. OAuth 2.0, the most widely used version, is simpler and more secure than OAuth 1.0. OAuth uses "access tokens" granted by the resource owner (user) to the third-party application. These tokens provide restricted access to the user’s resources hosted by the resource server without exposing the user's credentials.

Roles in OAuth:
- **Resource Owner**: The user who authorizes an application to access their account.
- **Client**: The application that wants to access the user's account.
- **Authorization Server**: The server that authenticates the resource owner and issues access tokens.
- **Resource Server**: The server hosting user data and capable of accepting and responding to protected resource requests using access tokens.

OAuth 2.0 defines several "grant types" (or "flows") for different use cases, like Authorization Code (for apps running on a web server), Implicit (for browser-based or mobile apps), Password Credentials, and Client Credentials.

Common use cases include allowing users to log into an application using their Facebook or Google account, granting applications access to their data on another service, etc. OAuth provides a more secure alternative to the traditional practice of users sharing their credentials with an application. It also reduces the risk for service providers as they don’t need to store user passwords.

OAuth allows the resource owner to define the scope of access granted to the client, which can be limited to specific actions, data types, or resources. For long-term access, OAuth may provide a refresh token that allows clients to obtain a new access token without user interaction.

