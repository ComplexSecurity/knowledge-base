Burp Scanner is a feature within [Burp Suite]() which is an integrated platform for performing security testing of web applications. Burp Scanner is a web vulnerability scanner that automates the process of detecting security vulnerabilities. It's designed to be used alongside manual testing and provides a comprehensive solution for web application security checks.

Burp Scanner automatically crawls and scans web applications for a wide range of security vulnerabilities. It performs both passive and active scans. 

1. Types of Scans:
	- **Passive Scanning**: Analyzes the application's traffic and identifies issues without sending any unusual requests or payloads.
	- **Active Scanning**: Proactively sends requests to the application, testing inputs and functionality for specific vulnerabilities.

Burp Scanner can detect various types of security issues, including [SQL injection](), [cross-site scripting]() (XSS), [Broken Authentication](), [path traversal](), and many others.

Before scanning, Burp Scanner crawls the application to map out the content and functionality. This crawl data is used to guide the active scanning process. Findings from the scanner can be further analyzed and exploited using other tools in the Burp Suite, such as [Burp Intruder](), [Burp Repeater](), and [Burp Extender]().

The scanner allows for significant customization of scan settings, enabling testers to tailor the scan to the specific application and to focus on particular areas or types of vulnerabilities. Burp Scanner generates detailed reports of its findings, which include information about the vulnerabilities, their severity, potential impact, and recommendations for remediation.

