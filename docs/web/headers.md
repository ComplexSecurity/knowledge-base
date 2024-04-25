The HTTP header is part of the [[HTTP Protocol|Hypertext Transfer Protocol]] (HTTP) and transmits additional information during HTTP requests or responses. In addition to the data that is delivered to a browser by the web server of the called website, server and browser exchange meta information about the document via the HTTP header.

An HTTP request contains a header area with information such as the date of the request, the referrer, or the preferred language. The HTTP response also contains a header field in which the server sends its information to the user's browser. This information exchange is usually invisible to the end user.

HTTP headers include fields which themselves consist of one line. Each line contains a name/value pair - called **key-value pair** - separated by a colon and is terminated by a line break.

Values that can be used for the HTTP header are defined in the RFC ("Requests for Comments"). In addition to the specified fields, there are also non-standard headers that can be used to add user-defined information. These headers usually start with an `X-`.

Some of the most common HTTP Headers include:

- **Accept** - defines the media types the [[client]] is able to accept from the [[server]]
- **User-Agent** - identifies the browser or client app making the request, enabling the server to tailor the response to the client.
- **Authorization** - used to send client's credentials to server when client is attempting to access a protected resource.
- **Content-Type** - identifies the media type of content in the request body.
- **Cookie** - client can use [[Cookies|cookies]] to send previously stored cookies back to the server.
- **Cache-Control** - controls caching behaviour in the client's browser or intermediate caches.
- **Server** - includes name and version of the server software that generated the response.
- **Set-Cookie** - instructs client to store a cookie with the specified name, value and additional attributes.
- **Content-Length** - specifies the size of the response body in bytes.

They can also be categorized and grouped together such as:

- **General Headers** - contextual and used to describe the message.
- **Entity Headers** - used to describe the content transferred by a message.
- **Request Headers** - used in an HTTP request and do not relate to the content.
- **Response Headers** - used in an HTTP response and do not relate to the content.
- **Security Headers** - class of response headers used to specify certain rules and policies to be followed.