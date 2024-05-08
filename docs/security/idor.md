IDOR stands for Insecure Direct Object References, a type of security vulnerability in web applications. IDOR occurs when an application provides direct access to objects based on user-supplied input. As a result, attackers can bypass authorization and access data and functionality they shouldn't have access to, such as other users' data or administrative functions.

A direct object reference occurs when an application exposes internal implementation objects, like files, database records, or key indexes, to users through its user interface or [APIs|API](). IDOR vulnerabilities arise when the application does not perform adequate authorization checks when these objects are accessed. An attacker can manipulate references to gain unauthorized access to data.

A typical example is a URL or a form parameter that includes a reference to an internal object, like `http://example.com/account?userid=123`. If proper authorization checks are not implemented, an attacker could change `userid=123` to another user's ID to access or modify their data.

IDOR can lead to [Sensitive Data Exposure|unauthorized data disclosure](), modification, deletion, and other security breaches. It can be especially damaging if sensitive data, like personal information, financial details, or administrative controls, are exposed.

Attackers typically exploit IDOR by manipulating parameters (such as URL query strings, [HTTP headers](), or POST data) and observing the resulting behavior to gain unauthorized access to data.

