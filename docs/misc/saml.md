SAML (Security Assertion Markup Language) is an open standard for exchanging authentication and authorization data between an [[Trusted Identity Provider (IdP)|identity provider (IdP)]] and a [[Service Provider (SP)]]. It is widely used for enabling [[Single Sign-On (SSO)]] for web applications, allowing users to log in once and gain access to multiple systems without needing to re-authenticate.

SAML is based on [[Extensible Markup Language|XML]] for data exchange and is used primarily for web-based authentication. The XML-based framework allows different systems to communicate authentication and authorization information securely.

Components of SAML:

- **Assertion**: This is the XML document that the identity provider sends to the service provider. It contains the authentication statement (proof of a user's identity), attributes (user information), and an optional authorization decision.
- **Identity Provider (IdP)**: The system or service that authenticates the user and sends the SAML Assertion to the service provider.
- **Service Provider (SP)**: The system or service that receives the SAML Assertion and provides access to the user based on the assertion.

This is how SAML works:

- A user attempts to access a resource or service (the service provider).
- The service provider requests an authentication assertion from the identity provider.
- The identity provider authenticates the user and sends a SAML Assertion back to the service provider.
- The service provider validates the assertion and grants access to the user.

SAML is commonly used to enable SSO, allowing users to log in with a single ID to gain access to a range of systems and applications, improving security and user experience. SAML supports various security measures, such as digital signatures and encryption, to ensure the integrity and confidentiality of the exchanged data.

Being an open standard, SAML can be implemented by various vendors, ensuring interoperability between different systems and applications for authentication and authorization. SAML is key in identity federation, enabling organizations to share identity information across multiple domains securely.

