Extensible Stylesheet Language Transformations (XSLT) Server-Side Injection is a web security vulnerability that occurs when an application accepts user input and unsafely processes it as part of an [[XSLT (Extensible Stylesheet Language Transformations)|XLST]] stylesheet.

XSLT is a language used for transforming [[Extensible Markup Language|XML]] documents into other formats, like [[HTML]], plain text, or other XML formats. If an application dynamically generates XSLT stylesheets based on user-supplied input without proper [[Input Sanitization|sanitization]] or validation, it can lead to this type of injection vulnerability.

XSLT is a powerful language used for transforming XML documents. It allows for complex manipulation and conversion of XML data into different document types. XSLT stylesheets define rules for how the transformation should occur.

The vulnerability arises when a web application includes user-controlled input in an XSLT stylesheet without proper sanitization. Malicious users can inject harmful XSLT code, which the server then processes. This process can potentially allow attackers to execute arbitrary code or commands on the server, access or modify sensitive data, or perform other malicious actions.

An attacker exploits this vulnerability by injecting malicious XSLT code into a point where the application accepts input, like a form or URL parameter. When the application processes this input as part of an XSLT transformation, the malicious code is executed.

Depending on the server’s configuration and the nature of the XSLT processor, impacts can range from unauthorized data disclosure to [[Knowledge Base/Remote Code Execution]].
