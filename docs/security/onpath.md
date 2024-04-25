On-path attackers place themselves between two devices (often a web browser and a web server) and intercept or modify communications between the two. The attackers can then collect information as well as impersonate either of the two agents. 

In addition to websites, these attacks can target email communications, [[DNS]] lookups, and public WiFi networks. Typical targets of on-path attackers include SaaS businesses, ecommerce businesses and users of financial apps.

You can think of an on-path attacker like a rogue postal worker who sits in a post office and intercepts letters written between two people. This postal worker can read private messages and even edit the contents of those letters before passing them along to their intended recipients.

In a more modern example, an on-path attacker can sit between a user and the website they want to visit, and collect their username and password. 

This can be done by targeting the [[HTTP Protocol|HTTP]] connection between the user and the website; hijacking this connection lets an attacker act as a proxy, collecting and modifying information being sent between the user and the site. 

Alternately the attacker can steal a user’s cookies (small pieces of data created by a website and stored on a user’s computer for identification and other purposes). These stolen cookies can be used to hijack a user’s session, letting an attacker impersonate that user on the site.

On-path attackers can also target DNS servers. In DNS on-path attacks such as [[DNS spoofing]] and [[DNS hijacking]], an attacker can compromise the DNS lookup process and send users to the wrong sites, often sites that distribute malware and/or collect sensitive information.