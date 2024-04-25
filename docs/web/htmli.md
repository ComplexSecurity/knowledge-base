HTML Injection, often known as "virtual defacements," is one of the easiest and most widespread vulnerabilities that occur when a web page neglects to sanitize user-supplied data or validate the output. 

As a result, the attacker can create his payloads and inject malicious HTML codes into the web application through the susceptible fields, allowing him to change the webpage content and even steal sensitive data.

Attackers often inject malicious [[JavaScript]], [[VBScript]], [[ActiveX]], and/or [[HTML]] into vulnerable applications to deceive the user in order to gather data from them.  

Cross-site scripting (XSS) vulnerabilities can be used by attackers to bypass authentication controls there by gaining access to sensitive data on your system. Well crafted malicious code can even help the attacker gain access to the entire system.

This vulnerability occurs when user input is not correctly sanitized and the output is not encoded. An injection allows the attacker to send a malicious HTML page to a victim. The targeted browser will not be able to distinguish (trust) legitimate parts from malicious parts of the page, and consequently will parse and execute the whole page in the victim’s context.

There is a wide range of methods and attributes that could be used to render HTML content. If these methods are provided with an untrusted input, then there is an high risk of HTML injection vulnerability. 

For example, malicious HTML code can be injected via the innerHTML JavaScript method, usually used to render user-inserted HTML code. If strings are not correctly sanitized, the method can enable HTML injection. A JavaScript function that can be used for this purpose is document.write().

