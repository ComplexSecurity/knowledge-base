Header Injection is a type of vulnerability in web applications where an attacker is able to inject malicious header values into [[HTTP Protocol|HTTP]] responses. This vulnerability typically occurs when user input is improperly sanitized before being included in the header output. It can lead to various security issues, including [[Cross-Site Scripting]] (XSS), website redirection, [[Web Cache Poisoning]], and [[Session Fixation]].

Header Injection involves injecting malicious content into HTTP response headers. By manipulating headers, an attacker can alter how the HTTP response is processed by the browser or intermediate proxies.

**Common Vulnerable Headers**:
- **Location Header**: Used for redirection. Injecting a malicious URL can redirect users to phishing or malware sites.
- **Set-Cookie Header**: Manipulating [[Cookies|cookie]] headers can lead to session fixation or hijacking.
- **Content-Type Header**: Altering the content type can change how the response is interpreted by the browser.

This vulnerability often arises when a web application incorporates user-supplied data into HTTP response headers without proper validation or escaping. For example, data from form inputs, query parameters, or cookies might be insecurely included in response headers.

In a web application, the following PHP code is vulnerable to header injection:

```php
header("Location: " . $_GET['url']);
```

If the `url` parameter is not properly sanitized, it can be exploited to redirect users to a malicious site.