Public Key Infrastructure (PKI) is a framework of policies, technologies, and procedures that provide secure electronic transactions and communication over networks. It utilizes [asymmetric cryptography](../cryptography/asym.md) to ensure secure data exchange and authentication. PKI is foundational to many aspects of digital security and trust.

At the heart of PKI are digital certificates, which are electronic documents used to verify the identity of entities (such as individuals, organizations, or devices) and associate them with a corresponding public key.

[CAs](../web/cas.md) are trusted entities that issue and manage digital certificates. They validate the identity of certificate applicants and issue certificates to affirm that identity.

PKI uses asymmetric encryption, which involves a pair of keys – a public key and a private key. The public key is shared openly, while the private key is kept secret. Data encrypted with a public key can only be decrypted with the corresponding private key, and vice versa.

PKI enables encryption for confidentiality and digital signatures for authentication and integrity. A digital signature is created using a private key and can be verified by anyone with the corresponding public key.

CRLs (Certificate Revocation Lists) are lists of certificates that have been revoked before their expiration dates, usually because the private key has been compromised or the user's credentials have changed.

Online Certificate Status Protocol (OCSP) is an alternative to CRLs for checking a certificate's revocation status. It provides real-time verification, which is more efficient than downloading CRLs.

PKI often involves a hierarchy of certificates. Root certificates are at the top of this hierarchy and are used to sign intermediate certificates, which in turn are used to sign end-user certificates. PKI establishes a chain of trust. If you trust the CA (and by extension, its root certificate), you can trust the certificates it has issued.

PKI is used in various applications, including securing web communications ([SSL/TLS](../cryptography/ssltls.md)), encrypting emails (S/MIME), authenticating users and devices in various systems, and ensuring secure transactions in e-commerce.


