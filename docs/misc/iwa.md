Integrated Windows Authentication (IWA) is a term used for a set of authentication protocols built into Microsoft Windows operating systems. It enables users to log in with their Windows credentials and gain access to network resources without being prompted to enter their credentials again. 

IWA uses the credentials of the user's current logon session to transparently authenticate the user to a network service or resource.

IWA provides [[Single Sign-On (SSO)|SSO]] capabilities, allowing users to access multiple services or applications within a Windows domain without needing to repeatedly enter their login credentials. IWA primarily uses the [[Kerberos authentication]] protocol for security but can fall back to [[NTLM]] (NT LAN Manager) in environments where Kerberos cannot be used.

By default, IWA encrypts the user's credentials and does not send them in plaintext across the network, reducing the risk of credential theft. IWA automatically authenticates users who are logged into a Windows domain when they access network resources, such as file shares or web applications, that support IWA.

A common example is an employee accessing an internal company web portal. When the employee, who is logged into their Windows domain account, opens the portal in a browser, IWA automatically authenticates their identity with the web server using their current session's credentials. The employee gains access to the portal without having to enter their username and password again.

