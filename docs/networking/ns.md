NS stands for ‘nameserver,’ and the nameserver record indicates which [DNS](dns.md) server is authoritative for that domain (i.e. which server contains the actual DNS records). 

Basically, NS records tell the Internet where to go to find out a domain's [IP address](ip.md). A domain often has multiple NS records which can indicate primary and secondary nameservers for that domain. Without properly configured NS records, users will be unable to load a website or application.

Here is an example of an NS record:

|example.com|record type:|value:|TTL|
|---|---|---|---|
|@|NS|ns1.exampleserver.com|21600|

!!! info
    Note that NS records can never point to a [DNS CNAME Records](cname.md)