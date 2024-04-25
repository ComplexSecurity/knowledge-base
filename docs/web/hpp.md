HTTP Parameter Pollution (HPP) is a web security vulnerability that occurs when a web application does not properly handle input with multiple parameters with the same name, leading to unexpected and potentially harmful behavior.

[[HTTP Protocol|HTTP]] requests can contain parameters that are used by web applications to perform actions or retrieve data. These parameters can be part of the [[Uniform Resource Locator|URL]] (in the case of GET requests) or in the body of the request (typically in POST requests).

In an HTTP Parameter Pollution attack, an attacker deliberately injects additional HTTP parameters or manipulates existing ones with the same name. The goal is to exploit the way the web application processes these parameters.

The impact of HPP depends on how the application handles multiple parameters with the same name. Some applications might take the first parameter value, others the last, while some might concatenate the values. This behavior can be exploited to manipulate the application's logic or access unauthorized data.

1. **Types of HPP**:
    - Local HPP: This occurs when the polluted parameter is used within the same application. It might lead to bypassing input validation checks, [[cross-site scripting]] (XSS), [[SQL injection]], etc.
    - Remote HPP: This involves polluting parameters that are built into URLs and then sent to other applications. It can be used to manipulate external systems or trick applications into generating malicious URLs.

Attackers can use HPP to modify the logic of an application, bypass security controls, or access unauthorized data. For example, if an application's access control depends on a parameter value, manipulating this value might grant higher privileges than intended.