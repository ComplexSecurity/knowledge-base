A Certificate Signing Request (CSR) is a request sent from an applicant to a [[Certificate Authorities (CAs)|Certificate Authority (CA]]) to apply for a digital identity certificate. It contains information that will be included in the certificate, such as the applicant's public key, organization name, common name (domain name), locality, and country.

The CSR is used in the process of obtaining an [[SSL certificates|SSL/TLS certificate]] for secure websites and other services that require encrypted data transmission.

The CSR includes the public key that will be included in the certificate. The corresponding private key is kept secure and is not transmitted. This includes the organization's name, the common name (e.g., a domain name for [[SSL]] certificates), and other identifying information. The CSR is signed by the applicant's private key. This signature is used by the CA to verify the authenticity of the request.

The applicant generates a private key and a CSR. The CSR is generated using software tools and is based on the private key. The applicant submits the CSR to a Certificate Authority. The CA verifies the identity and authority of the applicant. Once verified, the CA issues a certificate based on the CSR, which contains the applicant's public key and other information from the CSR.

An example of generating a CSR using OpenSSL:

1. Generate a private key:

```bash
openssl genrsa -out private.key 2048
```

This command creates a 2048-bit RSA private key and saves it in a file named private.key.

2. Generate a CSR:

```bash
openssl req -new -key private.key -out mycsr.csr
```

This command prompts for details like the common name (domain name), organization, country, etc., and creates a CSR (`mycsr.csr`) using the private key (`private.key`).
