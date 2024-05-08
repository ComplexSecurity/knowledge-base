Blind [Server-Side Request Forgery]() (SSRF) is a type of cybersecurity vulnerability where an attacker manipulates a server to make a request to a third-party system. 

In a "blind" SSRF attack, the attacker does not receive a direct response from the forged request. This makes it more challenging for the attacker to ascertain the success of the attack, but it also makes the attack harder to detect and prevent.

The attacker finds a vulnerable server that can make [HTTP Protocol|HTTP]() requests to other systems. This vulnerability typically arises when the server does not properly validate or restrict user-supplied URLs before using them in a web request.

The attacker crafts a request that, when processed by the server, causes it to make an unintended HTTP request to an external system. This external system could be another server on the internet or, more dangerously, a system within the server’s internal network.

In a blind SSRF attack, the attacker does not receive the response from the third-party system. This "blindness" means the attacker must use indirect methods to infer whether the attack was successful. For example, they might observe changes in the server's behavior or use other information sources.

Blind SSRF attacks can lead to information disclosure, internal network reconnaissance, interaction with internal services not directly accessible from the internet, and, in some cases, internal network attacks that can escalate to more serious intrusions.