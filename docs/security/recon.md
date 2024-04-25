Reconnaissance in the context of penetration testing and web hacking refers to the preliminary phase where attackers (or ethical hackers) gather information about their target to identify potential vulnerabilities and attack vectors. This phase is crucial as it lays the groundwork for subsequent stages of the attack or penetration test.

There are two types of recon:

1. **Passive Reconnaissance**: Involves collecting information without directly interacting with the target system. This is often preferred in the early stages to avoid detection.
2. **Active Reconnaissance**: Involves directly interacting with the target system to gather information. This can be more intrusive and might raise alerts if not done carefully.

Some examples of recon techniques include:

- Domain Name and IP Address Lookup: Gathering information about the domain names and associated IP addresses using tools like [[WHOIS]], [[nslookup]], or [[dig]].
- Network Scanning: Using tools like [[Nmap]] or Zmap to scan the network for open ports, running services, and detecting operating systems.
- Email Harvesting: Collecting email addresses related to the target organization through web scraping, social media, or other public sources.
- Social Engineering: Gleaning information from employees or stakeholders through [[social engineering]] tactics like pretexting or [[phishing]].
- Website Footprinting: Analyzing the target website for information like software versions, directory structure (using tools like [[Dirbuster]]), or [[Content Management System|CMS]] systems.
- DNS Enumeration: Extracting records, [[subdomains]], and other [[DNS]]-related information about the target.
- Public Record Searching: Looking through public records or open databases for information about the target organization.
- Social Media Analysis: Examining social media profiles related to the target for employee information, roles, and potential internal lingo or jargon that could be used in social engineering attacks.
- Google Hacking: Using advanced Google search techniques to uncover hidden information on the target’s website or associated pages.
- API Testing: Analyzing publicly exposed [[APIs]] for information leakage or vulnerabilities.
- SSL/TLS Certificate Analysis: Inspecting [[SSL certificates|SSL/TLS certificates]] for misconfigurations or vulnerabilities.
- Using Tools like Shodan or Censys: These search engines can find devices and systems exposed to the internet, providing a wealth of information about potential targets.

