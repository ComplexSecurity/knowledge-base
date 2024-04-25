Edge-Side Includes (ESI) Injection is a web security vulnerability that targets web caching systems using Edge-Side Includes, a markup language used for dynamic web content assembly at the edge of the network (i.e., in edge servers or [[Content Delivery Network|content delivery networks]]).

ESI is intended to optimize web traffic and reduce server load by allowing dynamic content to be assembled and updated independently of the static content on a webpage.

ESI tags are inserted into [[HTML]] documents to instruct a compatible web cache or edge server to take specific actions, like including content from another source or variable. When a client requests an ESI-enabled page, the server processes these ESI tags to assemble and deliver the final content.

ESI Injection occurs when an attacker is able to insert malicious ESI tags into content that will be processed by a caching server. This can happen if user input is not properly sanitized before being included in a web page that is then processed for ESI directives.

Depending on the capabilities of the ESI processor and the rights of the caching server, an attacker might use ESI Injection to perform actions like executing arbitrary code, manipulating cache content, or stealing sensitive information.

Consider a web application that includes user comments in a page without proper sanitization. An attacker could submit a comment containing ESI tags (`<esi:include src="..."/>`). If this input is processed by an ESI-capable cache, the injected tag could lead to the inclusion of malicious content or code.
