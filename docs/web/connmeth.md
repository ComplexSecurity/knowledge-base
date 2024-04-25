The `CONNECT` [[HTTP Protocol|HTTP]] method is used by the HTTP/1.1 protocol to establish a tunnel to a server identified by a given URI. It's primarily used for establishing connections that are then upgraded to [[TLS]] (Transport Layer Security), such as when a client communicates with an [[HTTPS Protocol |HTTPS]] server through an HTTP [[proxy]].

The `CONNECT` method is used to request that an intermediary (such as a proxy) establish a tunnel connection to the target server. For example, when a client wants to securely connect to an HTTPS website through an HTTP proxy, it sends a `CONNECT` request to the proxy with the hostname and port number of the HTTPS server.

```sql
CONNECT www.example.com:443 HTTP/1.1
```

Once the tunnel is established, the client can start a [[TLS handshake]] with the target server through the proxy, allowing secure communication.

Malicious users can potentially use the `CONNECT` method to bypass network restrictions or access controls by tunneling through proxies. For instance, they might access restricted websites or services through a corporate proxy.

If a web application includes a proxy server functionality, failing to properly restrict or monitor the use of the `CONNECT` method can lead to abuse. Attackers might use the proxy server to mask their IP address or conduct illegal activities. An attacker could use `CONNECT` to facilitate [[Man-in-the-Middle (MitM) attack|man-in-the-middle (MitM) attacks]], intercepting and possibly altering communications between a client and a server.
