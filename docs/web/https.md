HTTPS is the secure version of [[HTTP Protocol|HTTP]]. HTTPS is encrypted in order to increase security of data transfer. HTTPS uses an encryption protocol to encrypt communications. The protocol is called Transport Layer Security (TLS), although formerly it was known as Secure Sockets Layer (SSL).

The protocol secures communications by using what is known as an asymmetric public key infrastructure. This type of security system uses two different keys to encrypt communications between two parties:

- Private key - key is controlled by the owner of a website and it is kept private. It lives on the web server and used to decrypt information encrypted by the public key.
- Public key - key is available to everyone who wants to interact with the server in a way that is secure. Information encrypted by the public key can only be decrypted by the private key.

HTTPS prevents websites from having their information broadcast in a way that’s easily viewed by anyone snooping on the network. When information is sent over regular HTTP, the information is broken into packets of data that can be easily “sniffed” using free software. 

This makes communication over the an unsecure medium, such as public Wi-Fi, highly vulnerable to interception. In fact, all communications that occur over HTTP occur in [[Clear-Text|plain text]], making them highly accessible to anyone with the correct tools.

HTTPS is not a separate protocol from HTTP. It is simply using TLS/SSL encryption over the HTTP protocol. When a user connects to a webpage, the webpage will send over its SSL certificate which contains the public key necessary to start the secure session. The two computers, the [[client]] and the [[Server]], then go through a process called an SSL/TLS [[handshake]], which is a series of back-and-forth communications used to establish a secure connection.

