The `TRACE` HTTP method is a diagnostic method defined in the HTTP/1.1 protocol. Its primary purpose is to enable a client to see what is being received at the other end of the request chain and use that data for testing or diagnostic information. The `TRACE` method simply echoes back the received request so that a client can see any changes or additions made by intermediate servers.

When a `TRACE` request is made to a web server, the server responds with a message that includes the exact request that it received. This includes the request line, any headers, and the body of the request.

The `TRACE` method can present a web security risk, primarily through a type of attack known as [[Cross-Site Tracing (XST)]]:

- XST is an advanced form of [[Cross-Site Scripting|Cross-Site Scripting (XSS)]]. An attacker can exploit the `TRACE` method to steal cookies or other authentication information from browsers. This is especially concerning if the [[HttpOnly flag]] is not set on cookies, as an XST attack can be used to bypass this protection. The attacker crafts a malicious script that forces the victim's browser to send an HTTP TRACE request to the server. The response to this TRACE request includes the victim's cookies and other header information, which the script then captures.
- The `HttpOnly` flag is used to protect cookies from being accessed by client-side scripts. However, if an application supports the `TRACE` method, it might be possible for an attacker to use XST to bypass this protection and access `HttpOnly` cookies.


