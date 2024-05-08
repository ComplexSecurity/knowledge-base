**Server-Side Request Forgery** (SSRF) is a web security vulnerability that allows an attacker to induce the server-side application to make [HTTP Protocol|HTTP]() requests to an arbitrary domain of the attacker's choosing. This vulnerability occurs when a web application fetches a remote resource without sufficiently validating the user-supplied [Uniform Resource Locator|URL]().

Server-side request forgery is a web security vulnerability that allows an attacker to cause the server-side application to make requests to an unintended location.

In a typical SSRF attack, the attacker might cause the server to make a connection to internal-only services within the organization's infrastructure. In other cases, they may be able to force the server to connect to arbitrary external systems. This could leak sensitive data, such as authorization credentials.

In an SSRF attack, the attacker has limited direct control over the server but can manipulate the server to perform certain actions, make requests, or send data on their behalf.

SSRF typically exploits a vulnerability in a web application that allows the attacker to manipulate the URLs that the [server]()-side application accesses.

The impact of SSRF can be significant, ranging from unauthorized access to internal services, [Sensitive Data Exposure|information disclosure](), and interaction with internal network infrastructure that might otherwise be inaccessible from the outside. In some cases, SSRF can be used to carry out more sophisticated attacks like port scanning, attacking internal applications, or accessing sensitive data.

There are two types of SSRF attacks:

- **Basic SSRF** - The attacker causes the server to make a request to a domain of their choice. The response from the requested server might be returned to the attacker, allowing them to read sensitive data.
- [Blind SSRF]() - The attacker does not receive the response directly. They might infer the success of the attack by observing changes in the application's behavior or by leveraging other information sources.