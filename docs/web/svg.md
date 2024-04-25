SVG (Scalable Vector Graphics) content refers to SVG elements or scripts embedded within SVG files that are used for malicious purposes, particularly in the context of web security. 

SVG is an [[Extensible Markup Language|XML]]-based vector image format, and like any other XML or [[HTML]]-like data, it can be used to execute [[JavaScript]] or other types of code, leading to security vulnerabilities such as [[Cross-Site Scripting]] (XSS) attacks.

SVG files can contain JavaScript, which might be executed when the SVG is rendered. For instance, the \<script> tag within an SVG can execute JavaScript in the context of the user's browser.

SVGs can contain links, which can be used in phishing attacks. For example, using the \<a> tag within an SVG, an attacker might trick users into clicking a link that leads to a malicious website.

SVGs can carry embedded payloads, like XSS attacks, that are triggered when the SVG is rendered. This can include using attributes like onload or onerror to trigger JavaScript execution.

Since SVG is XML-based, it can be used to exploit vulnerabilities in XML parsers, such as [[XML External Entities (XXE)]] attacks, where external entities are referenced within the SVG to access local files or remote resources.

Tools like [[DOMPurify]] can clean SVG content, removing potentially harmful scripts or tags.