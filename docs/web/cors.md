Cross-Origin Resource Sharing (CORS) is a security feature in web browsers that controls how web pages in one domain can request resources from another domain.

It's a crucial part of modern web security, designed to allow safe, controlled access across different origins while protecting against certain types of web attacks, such as [[Cross-Site Scripting]] (XSS) and data theft.

In web security, an "origin" is defined by the scheme (protocol), host (domain), and port of a [[Uniform Resource Locator|URL]]. For example, `https://example.com` and `https://sub.example.com` are different origins.

By default, web browsers enforce a [[Same Origin Policy]] (SOP), which restricts web pages from making requests to a different domain than the one that served the web page. This policy is a crucial security mechanism that prevents malicious scripts on one page from obtaining access to sensitive data on another web page through the browser.

Modern web applications often need to make requests to different domains for resources like [[APIs]], fonts, or images. CORS provides a way to safely allow these cross-origin requests.

CORS relies on specific [[HTTP headers]]. The most important is the **Access-Control-Allow-Origin** header, which the server includes in the response to indicate whether the requesting origin is permitted to access the resource

For certain types of requests (like those using custom headers or [[HTTP Verbs|HTTP methods]] other than GET or POST), the browser sends a pre-flight request - it is an OPTIONS request to the server before the actual request, asking if it is okay to send the actual request.

To support CORS, the server hosting the resources must be configured to send the appropriate headers. Without these headers, the browser will block the cross-origin request.

CORS provides security by allowing servers to specify who can access their resources and under what conditions. It doesn’t weaken security; rather, it enables controlled access while maintaining the protection provided by the same-origin policy.
