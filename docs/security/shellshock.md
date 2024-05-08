Shellshock, also known as the Bash bug, is a critical vulnerability in the [Bash]() shell.

It affects all operating systems (Linux and Unix based), which allows an attacker to execute arbitrary commands on a vulnerable system by sending specially crafted environment variables to a Bash-based application.

It is a severe threat to the system and causes extreme data breaches. If this vulnerability is successfully exploited, an attacker can remotely issue commands on the target host, i.e., [Knowledge Base/Remote Code Execution|remote code execution (RCE)](). 

Though Bash is not an Internet-facing service, many network and internet services (for example, web servers) use environment variables for communicating with the server’s OS.   

If environment variables not sanitized before execution, an attacker can send commands through [HTTP Protocol|HTTP]() requests and get them executed by the server’s OS. 



