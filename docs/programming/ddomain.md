document.domain is a property in [JavaScript](../programming/js.md) that gets or sets the domain of the current document. This property is part of the [Document Object Model (DOM)](../web/dom.md) and is used primarily in the context of the [Same Origin Policy](../web/sop.md), which is a critical security concept in web development.

Web browsers implement the Same-Origin Policy to prevent potentially malicious scripts on one page from accessing data or code on another page with a different origin. An origin is defined by the scheme (protocol), host (domain), and port of a URL.

For two pages to interact with each other's content via JavaScript, they need to have the same origin.

By setting document.domain to a specific value, you can loosen the restrictions imposed by the Same-Origin Policy. This is particularly useful when you have two different subdomains that need to interact with each other.

An example to get the domain may be:

```javascript
var domain = document.domain;
```

An example of setting the domain may be:

```javascript
document.domain = "example.com";
```

Modifying document.domain can have security implications. Reducing the restrictions of the Same-Origin Policy should be done carefully as it can potentially expose your website to certain types of attacks, such as [Cross-Site Scripting (XSS)](../web/xss.md).

Modern web development practices often favour more secure alternatives for cross-origin communication, such as [Cross-Origin Resource Sharing (CORS)](../web/cors.md) and postMessage API. These methods provide more controlled and secure ways to handle cross-origin interactions.
