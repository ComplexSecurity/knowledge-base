The `HttpOnly` [[Cookies|cookie]] flag is a directive used when setting HTTP cookies to help mitigate the risk of client-side script access to the protected cookie. This flag is set by the server when sending the `Set-Cookie` HTTP header and instructs the web browser to restrict access to the cookie from client-side scripts.

The primary purpose of the `HttpOnly` flag is to provide a security measure against [[cross-site scripting]] (XSS) attacks. By marking the cookie as `HttpOnly`, it ensures that the cookie cannot be accessed through client-side scripting languages like [[JavaScript]]. 

This means that even if a script injection vulnerability exists in the website, the attacker cannot easily steal `HttpOnly`-protected cookies via JavaScript. It's an additional layer of security for session cookies and other sensitive cookies, as it helps to prevent unauthorized access and exfiltration of cookie values.

When a server sets a cookie, it can add the `HttpOnly` flag in the `Set-Cookie` HTTP header:

```css
Set-Cookie: sessionId=abc123; HttpOnly
```

In this example, the `sessionId` cookie is marked as `HttpOnly`, which means it will not be accessible via JavaScript running in the browser (e.g., through `document.cookie`). While the `HttpOnly` flag is a valuable tool for mitigating the impact of XSS attacks, it is not a complete solution. It does not prevent the attacks themselves but limits what an attacker can do, particularly with regard to stealing cookies.

To maximize security, `HttpOnly` should be used in conjunction with other flags like [[Secure Flag|Secure]] (which ensures cookies are sent only over [[HTTPS Protocol|HTTPS]]) and proper input validation techniques to prevent XSS vulnerabilities in the first place.





