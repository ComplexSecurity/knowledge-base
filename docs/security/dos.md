DoS, or Denial of Service attacks, are cyber attacks aimed at disrupting the normal functioning of a targeted server, service, or network by overwhelming it with a flood of internet traffic. DoS attacks achieve this by utilizing one computer and an internet connection, often targeting the infrastructure of a web application.

During penetration testing, testers may assess how resilient a web application is to DoS attacks. This involves simulating DoS scenarios to evaluate the robustness of the web application and its supporting infrastructure.

Part of penetration testing can include stress testing the web application to see how much traffic it can handle before becoming unresponsive. Penetration testers aim to identify specific components (like [[APIs]], server configurations, [[Databases (KB)]]) that could be potential bottlenecks or vulnerabilities under heavy load.

Testers might verify the effectiveness of strategies in place to mitigate Distributed Denial of Service (DDoS) attacks, where the attack comes from multiple sources.

Automated tools used for scanning and [[Web Crawling|crawling]] a website can generate a high volume of requests in a short time. This can overload the server, especially if it's not equipped to handle such traffic.

Additionally, testing for certain vulnerabilities (like [[SQL injection]], or [[XML External Entities (XXE)]] attacks) might involve operations that are unexpectedly resource-intensive for the server, leading to a slowdown or crash.
