DOMPurify is a [JavaScript](../programming/js.md) library designed to sanitize [HTML](../web/html.md) and prevent [Cross-Site Scripting (XSS)](../web/xss.md) attacks. XSS attacks involve injecting malicious scripts into web pages viewed by other users, exploiting the trust a user has for a particular site.

DOMPurify mitigates this risk by sanitizing HTML content, ensuring that it's safe to insert into the DOM ([Document Object Model](../web/dom.md)).

It removes harmful HTML, JavaScript, [SVG](../web/svg.md), and MathML content from user input, ensuring that only clean, safe content is rendered by the browser.

DOMPurify is particularly useful in applications that allow user-generated content, where there is a risk of XSS attacks. For instance, in forums, comment sections, or any web application that dynamically inserts HTML content based on user input.

When you pass a string of HTML to DOMPurify, it parses the HTML and removes any elements or attributes that could be used for XSS. This includes <script\> tags, javascript: URLs, event handler attributes (like onclick), and many others.

The result is a sanitized version of the HTML that is safe to insert into the DOM.

DOMPurify is easy to integrate into web projects. It can be included as a standalone script, or installed via package managers like npm for use in larger JavaScript applications. It's commonly used in conjunction with libraries like [ReactJS](../frameworks/reactjs.md), [AngularJS](../frameworks/angularjs.md), or [Vue.js](../frameworks/vue.md) to sanitize dynamic content.
