HTTP verb tampering is a type of web security vulnerability that occurs when a web server incorrectly handles [[HTTP Verbs|HTTP methods]] or verbs. This vulnerability arises when the server is configured to respond differently to various HTTP methods, but does not properly restrict or validate these methods for different resources. 

Attackers can exploit this vulnerability by using unexpected or less commonly used HTTP methods (such as [[PUT HTTP Method|PUT]], [[DELETE HTTP Method|DELETE]], [[TRACE HTTP Method|TRACE]], [[CONNECT HTTP Method|CONNECT]], etc.) to bypass security controls, access unauthorized content, or perform unauthorized actions.

Some common HTTP methods:

- **GET**: Retrieve data from the server.
- **POST**: Send data to the server to create/update a resource.
- **PUT**: Replace all current representations of the target resource with the request payload.
- **DELETE**: Remove the specified resource.
- **HEAD**: Similar to GET, but it retrieves only the header information and not the body of the response.
- **OPTIONS**: Describe the communication options for the target resource.
- **TRACE**: Perform a message loop-back test along the path to the target resource.
- **CONNECT**: Establish a tunnel to the server identified by the target resource.

Suppose a web application correctly restricts sensitive actions to POST requests (like form submissions) but does not similarly restrict GET requests. An attacker might be able to perform the same actions by crafting a GET request with the same parameters, bypassing any server-side checks that are only applied to POST requests.

A website might only check for GET and POST methods and restrict certain actions to these methods. However, the server might still accept other methods like PUT or DELETE. An attacker could use these methods to modify (PUT) or delete (DELETE) content on the server if proper checks are not in place.

If the TRACE method is enabled, an attacker might use it to perform a [[cross-site scripting]] (XSS) attack. The attacker could trick a victim into sending an HTTP TRACE request with a malicious script in the headers. The server’s TRACE response would include this script, which could then be executed in the context of the victim’s browser.

Imagine a web application that manages blog posts. The application allows users to create, edit, and delete their blog posts. To simplify the scenario, let's assume the application uses the following HTTP methods:

- `POST` to create a new blog post.
- `PUT` to edit an existing blog post.
- `DELETE` to remove a blog post.

However, due to a misconfiguration or oversight in security, the application does not properly enforce access control on the `DELETE` method. An attacker discovers that while the application properly checks user permissions for `POST` and `PUT` requests, it does not do so for `DELETE` requests. This means any authenticated user can delete any blog post, even if they don't have permission to do so.

Here's an example of how an attacker might exploit this vulnerability using a simple HTTP request. This could be done using a tool like [[cURL]]:

```bash
curl -X DELETE "http://example.com/blogpost?id=123" -H "Cookie: sessionid=valid_user_session"
```

- `-X DELETE`: Specifies the HTTP method to use, which is `DELETE` in this case.
- `"http://example.com/blogpost?id=123"`: The URL of the blog post to delete. The attacker targets blog post with ID `123`.
- `-H "Cookie: sessionid=valid_user_session"`: Includes a header with a valid session ID to authenticate as a legitimate user.

For mitigation tactics:

- **Proper Configuration**: Configure the server to allow only necessary HTTP methods for each resource. Unnecessary methods like TRACE or CONNECT should be disabled if not needed.
- **Input Validation**: Implement strict input validation on the server side to ensure that only appropriate actions are taken for each HTTP method.
- **Security Checks**: Apply consistent security checks across all HTTP methods to prevent bypassing controls by simply changing the method.
- **Testing**: Regularly test web applications for HTTP method vulnerabilities using tools and techniques like penetration testing.

