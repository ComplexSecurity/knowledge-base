The `Secure` cookie flag is an option used when setting [[HTTP Protocol|HTTP]] [[cookies]] to ensure that the cookie is sent only over secure [[HTTPS Protocol|HTTPS]] connections. This flag is an important security feature for web applications, as it helps prevent the cookie from being exposed to [[Man-in-the-Middle (MitM) attack|man-in-the-middle (MitM) attacks]].

When a cookie is set with the `Secure` flag, it instructs the web browser to only send the cookie if the connection is HTTPS. This prevents the cookie from being sent over unencrypted HTTP connections, where it could be easily intercepted and stolen. The flag is crucial for protecting sensitive information contained in cookies, like session IDs or authentication tokens, from being exposed over non-secure channels.

When a server sets a cookie, it can include the Secure flag in the Set-Cookie HTTP header:

```css
Set-Cookie: sessionId=abc123; Secure
```

In this example, the `sessionId` cookie is marked as `Secure`, indicating that the browser should only send it over an HTTPS connection. 

For enhanced security, the `Secure` flag is often used in conjunction with the [[HttpOnly Flag|HttpOnly]] flag, which prevents the cookie from being accessed via client-side scripts. Implementing the `Secure` flag requires that the website supports HTTPS. All requests should be served over HTTPS to ensure that cookies are always transmitted securely.

While the `Secure` flag is essential for protecting cookies during transmission, it does not prevent other types of attacks like cross-site scripting (XSS). Therefore, it should be part of a comprehensive security strategy.
