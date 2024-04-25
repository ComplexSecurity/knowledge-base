  
SSL stripping is a type of [[Man-in-the-Middle (MitM) attack|man-in-the-middle (MITM)]] attack where the attacker intercepts and alters the communication between a user's browser and a web server to force the connection to downgrade from a secure [[HTTPS Protocol|HTTP]] connection to an unsecure [[HTTP Protocol|HTTP]] connection. 

This attack exploits the fact that many websites redirect from an initial HTTP connection to a secure HTTPS connection. By intercepting and manipulating this redirect, the attacker can keep the connection unencrypted, allowing them to read and modify any data passed between the two parties.

The user attempts to connect to a website (e.g., a banking website) using HTTP. The attacker, positioned between the user and the website, intercepts this request. Instead of allowing the website to redirect the user to the secure HTTPS version, the attacker sends an unencrypted version of the site to the user, usually by stripping the "s" from "https://" in the redirection response.

The user, unaware of the switch, sends sensitive information (like login credentials) over the unsecure HTTP connection. The attacker captures this unencrypted data, which can include personal, financial, or login information.

Consider a user, Alice, who wants to log in to her online banking account:

1. **Alice's Action**: Alice types `http://www.mybank.com` into her browser and hits enter.
2. **Interception by Attacker**: A hacker, who has already infiltrated the network Alice is using (e.g., a public Wi-Fi), intercepts the request.
3. **SSL Stripping**: Instead of allowing `http://www.mybank.com` to redirect Alice to `https://www.mybank.com`, the attacker strips the response of its secure HTTPS redirect, forcing Alice’s browser to stay on the HTTP version of the site.
4. **Alice’s Unawareness**: Alice sees the bank’s login page (which is actually a non-secure version presented by the attacker) and enters her username and password.
5. **Data Theft**: The attacker captures Alice's credentials sent over HTTP, gaining unauthorized access to her bank account.

