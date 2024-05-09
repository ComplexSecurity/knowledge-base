Burp Intruder is a tool within the [Burp Suite](../tools/burpsuite.md), which is a popular set of tools used for web application penetration testing. Burp Intruder is specifically designed for automating customized attacks against web applications. It is widely used for tasks such as enumerating identifiers, harvesting useful data, and fuzzing for vulnerabilities.

Burp Intruder can automate the process of submitting multiple HTTP requests to a web application. It is highly configurable and can be used to customize the payload and the behavior of each request.

1. Key Features and Use Cases:
    - **Brute Force Attacks**: Testing login forms or other input fields where attackers might attempt to guess credentials or identifiers.
    - **Parameter Fuzzing**: Automatically varying the values of parameters to test how a web application responds to unexpected or malicious input.
    - **Enumeration**: Identifying valid usernames, IDs, or other specific data by automating requests with different input values.
    - **Data Harvesting**: Extracting useful data from responses, such as error messages or informative headers.

Burp Intruder supports a wide range of payload types, including simple lists, numbers, dates, and custom payloads. It can generate payloads or use predefined or custom lists. Burp Intruder offers various attack types, such as Sniper, Battering Ram, Pitchfork, and Cluster Bomb, each suitable for different scenarios and objectives.

The responses to the Intruder requests can be reviewed within the tool, which provides functionalities to analyze and filter the results. This helps in identifying interesting patterns or anomalies in the responses.

Being part of the Burp Suite, Burp Intruder can work in tandem with other tools in the suite, like [Burp Repeater](../tools/repeater.md) and [Burp Scanner](../tools/scanner.md), for more comprehensive testing. While powerful, Burp Intruder can be resource-intensive, especially when performing large numbers of requests. Efficiency can be managed through settings like request throttling.

