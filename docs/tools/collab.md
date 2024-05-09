Burp Collaborator is a feature in the [Burp Suite](../tools/burpsuite.md), a popular web application security testing tool. Burp Collaborator is designed to assist security professionals and penetration testers in identifying and exploiting security vulnerabilities in web applications. 

Burp Collaborator facilitates out-of-band interaction with external systems during web application testing. It helps testers identify interactions initiated by the target application that may not be directly visible in the application's responses. 

Some security vulnerabilities, such as blind [SQL injection](../security/sqli.md), may not directly expose results in the application's responses. Burp Collaborator helps in detecting these blind vulnerabilities by establishing connections to a unique external server controlled by the tester.

Burp Collaborator uses both [DNS](../networking/dns.md) interactions and [HTTP](../web/http.md) interactions to communicate with its external server. DNS interactions involve subdomains, while HTTP interactions may include making HTTP requests to a unique domain or [IP address](../networking/ipa.md) controlled by Burp Collaborator.

Burp Collaborator is integrated with various tools within the Burp Suite, such as the [Scanner](../tools/scanner.md), [Intruder](../tools/intrude.md), and [Repeater](../tools/repeater.md). This integration allows testers to leverage the Collaborator's capabilities during different phases of the testing process.

Burp Collaborator can be set to automatically interact with the target application during various testing activities. Additionally, testers can manually initiate interactions to gather specific information. Burp Collaborator helps in detecting potential data exfiltration channels by monitoring the interactions initiated by the target application.

Burp Collaborator provides detailed logs and documentation of interactions, allowing testers to analyze and understand the communication patterns between the target application and external systems.