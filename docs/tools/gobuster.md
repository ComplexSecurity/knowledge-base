GoBuster is a tool used in cybersecurity, particularly in the field of penetration testing and ethical hacking. It is designed for brute-forcing [[Uniform Resource Locator|URIs]] (directories and files) in web applications, [[DNS]] [[subdomains]], and Virtual Host names (VHOSTs). 

This tool is developed in Go (Golang) and is favored for its speed and efficiency.

It can discover hidden directories and files on a web server by trying different paths (URIs) against the target. This is useful for finding potentially unlisted pages or directories that may contain sensitive information.

GoBuster can be used to find subdomains of a given domain. This is done by brute-forcing DNS using a wordlist, helping to uncover hidden or unadvertised subdomains. 

It can brute-force virtual host names (VHOSTs) on a server. This is particularly useful when dealing with web servers hosting multiple domains (virtual hosts) on the same [[IP address]].