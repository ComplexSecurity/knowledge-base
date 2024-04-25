Content Security Policy (CSP) is a security mechanism used to define a list of trusted sources for content that a website or a specific web page is allowed to load, as well as what protocol will be used for that. This can include scripts, stylesheets, images, and other types of content that can be embedded into a web page.

Content Security Policy is a powerful defense in depth security control that helps block unauthorized requests for content located outside of the current website. In addition to this, CSP successfully prevents the execution of inline scripts and restricts unsafe dynamic code execution.

As an [[HTTP Protocol|HTTP]] security response header, CSP passes the instructions configured by the website owner to the visitor’s browser.

The browser, then, must follow the instructions and block the delivery of content that was not authorized by the Content Security Policy rules. This way, the browser will see that certain content was referenced by a web page but will refuse to load it.

The Content Security Policy (CSP) is a protection standard that helps secure websites and applications against various attacks, including data injection, [[Clickjacking]], and [[cross-site scripting]] attacks.

CSP implements the [[Same Origin Policy]], ensuring that the browser only executes code from valid sources. Developers can use precisely-defined CSPs to eliminate common attack vectors by defining the content sources. This article explores a content security policy and how a CSP header can help prevent common vulnerabilities.
