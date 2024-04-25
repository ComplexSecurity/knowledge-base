SSL, short for Secure Sockets Layer, is a standard security technology for establishing an encrypted link between a web server and a browser. This secure link ensures that all data transmitted between the web server and browser remains private and integral. SSL is a critical technology for securing internet connections and protecting sensitive data from being intercepted by attackers.

SSL provides encryption for data in transit, which means that any information exchanged between the user and the website cannot be read by anyone else. SSL also involves authenticating the server to the client, typically through [[SSL certificates]]. This ensures that users are communicating with the intended website and not a malicious site.

Websites use SSL certificates to establish their identity. These certificates are issued by [[Certificate Authorities (CAs)]] and contain the website's public key and the identity of the website. When a user connects to an SSL-secured website, an "[[SSL Handshake]]" occurs, where the server and browser establish the encryption parameters for the session.

How it works:

- When a user accesses an SSL-secured website (indicated by [[HTTPS Protocol|HTTPS]] in the URL and often a padlock icon in the browser), the browser requests the server's SSL certificate.
- The server sends its certificate, including its public key.
- The browser checks the certificate against a list of trusted CAs and ensures that the certificate is valid, has not expired, and is being used by the website for which it has been issued.
- If the certificate is valid, the browser uses the server’s public key to encrypt data and send it to the server.
- The server decrypts the data using its private key, and the secure session begins.

Although SSL is still widely used as a term, the SSL protocol itself is considered outdated and has been replaced by [[TLS]] (Transport Layer Security). TLS is an improved version of SSL and addresses various security issues found in the earlier SSL protocols. Despite this, the term SSL continues to be commonly used to refer to both SSL and TLS technologies.

It is essential for protecting data as it moves between servers and clients, particularly for websites that handle sensitive data like credit card information, personal data, and login credentials. Websites with [[SSL-TLS|SSL/TLS]] are often viewed as more trustworthy by users. Modern browsers also warn users when they are about to access a website that is not secured by SSL/TLS.
