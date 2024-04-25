The hosts file is a simple text file used by the OS to map [[Hostname|hostnames]] to an [[IP Address]]. Before a device reaches out to the Internet to find the IP address of a website, it first checks the hosts file to see if there is an entry for that hostname.

You can manually add entries to the hosts file. Each entry must contain an IP address and the corresponding hostname. An example entry is as follows:

```powershell
127.0.0.1 login.fakedomain.com
```

Above, any request for login.fakedomain.com will be sent to 127.0.0.1 instead of looking it up via DNS. It's often used in local network environments, for testing websites, or for blocking access to websites.

It is also often used in hacking to specify a manual entry for a website or subdomain that may not be accessible over the Internet, and therefore has no entry in a [[DNS]] server.

