A token in a URL vulnerability refers to a security risk that arises when sensitive information, such as authentication tokens, session identifiers, or other confidential data, is included in a URL. This practice can lead to several security issues due to the way URLs are handled and transmitted over the internet.
  
URLs are often stored in the browser's history. If a URL contains sensitive tokens, they could be exposed to anyone with access to the user's browser history. When a user clicks on a hyperlink, the browser typically sends the [Uniform Resource Locator|URL]() of the current page (which may contain the token) in the [HTTP Protocol|HTTP]() referer header to the target site. This can inadvertently leak the token to third parties.

URLs are commonly logged by web servers. If a URL with a token is logged, the token could be exposed in server logs, which might be accessible to unauthorized personnel or could be inadvertently shared. 

In non-[HTTPS Protocol|HTTPS]() (unencrypted) connections, the entire URL, including the token, can be intercepted by anyone who can snoop on the network traffic. Users often share URLs, not realizing they may be sharing their session or other sensitive information embedded in the URL.

Imagine a web application that uses URL parameters for session management, like this:

```html
http://example.com/dashboard?token=abc123
```

In this scenario, `abc123` is a session token. If an attacker gains access to this URL (via browser history, network sniffing, server logs, etc.), they could hijack the user's session.