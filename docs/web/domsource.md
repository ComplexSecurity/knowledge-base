In the context of the [[Document Object Model]] (DOM), "sources" refer to methods or properties that can read data from potentially untrusted or unsafe sources. This data might include user inputs, URL parameters, responses from external APIs, or any other data that the web application processes.

Some examples include:

- document.URL - contains the [[Uniform Resource Locator|URL]] of the current document
- document.cookie - provides access to the cookies associated with the document
- document.referrer - indicates the address of the webpage that linked to the current page
- location.search - contains the query string part of the URL
- User input fields like text boxes or text areas

The primary risk associated with DOM sources is the potential for this data to be manipulated or crafted in a malicious way. If not properly handled, such data can be used in [[Cross-Site Scripting|XSS]] attacks.
