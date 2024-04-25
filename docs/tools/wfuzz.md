Wfuzz is a flexible tool for [[Brute Force Attack|brute forcing]] internet resources. It's widely used in penetration testing and ethical hacking to discover hidden resources on web servers. Unlike many other tools, Wfuzz is known for its versatility and ability to be tailored for different tasks.

Wfuzz can be used to brute force various web elements, including [[Uniform Resource Locator|URLs]], parameters, forms, [[HTTP Headers|headers]], and [[cookies]]. It also allows for the injection of payloads at multiple points, making it possible to test input vectors in GET and POST requests, cookies, headers, file uploads, and more.

Wfuzz allows testers to identify resources based on the server's response (like [[HTTP response codes]], response length, or response time). This makes it easier to identify valid resources even when there's no clear indication in the server's response text.

A simple example may be:

```bash
wfuzz -c -z file,wordlist.txt --hc 404 http://target-site/FUZZ
```

- `-c`: Colorize the output for better visibility.
- `-z file,wordlist.txt`: Use the "wordlist.txt" file as a source of fuzzing payloads.
- `--hc 404`: Ignore HTTP responses with a status code of 404 (not found).
- `http://target-site/FUZZ`: Specify the target URL where "FUZZ" will be replaced with payloads from the wordlist.

!!! info
WFuzz will attempt to access different directories and files on the target web server by replacing "FUZZ" with each word from the "wordlist.txt" file. If a directory or file exists, it will return a valid HTTP response code (e.g., 200). The tool reports the discovered directories and files.
