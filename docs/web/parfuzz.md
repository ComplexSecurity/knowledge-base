Parameter fuzzing, also known as web parameter tampering or input fuzzing, is a technique used in cybersecurity and web application testing. It involves manipulating or "fuzzing" the parameters of a web application to test for vulnerabilities.

The goal is to identify potential security flaws in web apps by testing how they handle unexpected or malicious input, including testing for vulnerabilities like [[SQL injection]], [[Cross-Site Scripting]], [[Command Injection]], [[Buffer Overflows]] and more.

Some common parameters that are fuzzed include:

- [[Uniform Resource Locator|URL]] parameters - values in the query string of a URL
- Form fields - inputs in web forms, including hidden fields
- [[Cookies]] - data stored on the client-side and sent with requests
- [[HTTP Headers]] - information sent in request and response headers

The process involves changing these parameters and observing the app's response, including techniques like:

- Injecting special characters - entering characters like quotes, backslashes and semicolons
- Overloading inputs - providing unexpected long strings or large amounts of data
- Using known malicious inputs - injecting payloads known to exploit certain vulnerabilities

There are various tools to automate the process such as [[Ffuf]].

