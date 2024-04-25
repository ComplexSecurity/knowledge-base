Open redirects are a security vulnerability that occurs when a web application or server is configured to automatically redirect users to a specified URL without adequately validating that URL. This flaw can be exploited by attackers to redirect users to malicious websites, often as part of [[phishing]] attacks.

In an open redirect scenario, the application accepts a URL as a parameter and then redirects the user to this URL. If the application doesn't properly validate this URL, it can redirect users to any site, including malicious ones. Attackers exploit this by crafting URLs that include the legitimate website's domain followed by a redirect instruction to a malicious site. To an unsuspecting user, the URL appears trustworthy because it starts with a known, legitimate domain.

Consider a website `example.com` with a login page that, after successful login, redirects users to the page they were initially trying to visit. This is a common and legitimate use of redirection. The URL might look like this:

```http
https://www.example.com/login?redirect=www.example.com/dashboard
```

In an open redirect vulnerability scenario, an attacker could craft a URL like:

```http
https://www.example.com/login?redirect=www.malicious.com
```

If `example.com` doesn't properly validate the `redirect` parameter, it will redirect the user to `malicious.com` after login, potentially leading to phishing, malware infection, or other malicious activities.

Attackers can trick users into believing they are visiting a trusted site while actually directing them to a malicious one. Users can be redirected to sites that host malware, leading to potential infections. Exploiting open redirects can damage the reputation of the legitimate site that is used for redirection.

