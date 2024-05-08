Session hijacking is a type of cyber attack where an attacker takes control of a user's session to gain unauthorized access to information or services in a computer system. In the context of web applications, it often involves the compromise of a session token, which is used to authenticate a user after they have logged in. 

When a user logs into a web application, a session is established between the user's browser and the web server. This session is usually identified by a session token (like a [Cookies|cookie]()) that is unique to each user session.

The attacker's goal is to capture this session token. This can be done through various methods such as [Packet Sniffing]() on unsecured networks, [cross-site scripting]() (XSS) attacks, or exploiting other security vulnerabilities.

Once the attacker has the session token, they can use it to impersonate the legitimate user. Since the session token is what authenticates the session after login, the attacker doesn't need the user's password.