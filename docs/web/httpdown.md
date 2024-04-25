An HTTP downgrade attack is a cyber attack where an attacker intercepts the communication between a user's browser and a website, forcing the connection to revert from a secure [[HTTPS Protocol|HTTPS]] connection to an unsecured [[HTTP Protocol|HTTP]] connection.

In general, any system that employs any form of backward compatibility can be susceptible to a downgrade attack. The balance between maximum utility and maximum security is a difficult one to strike: however tempting it may be to enforce your visitors to keep their systems updated, you want people to be able to access your server using older technology.

Downgrade attacks can take many forms, but they all have a few elements in common. Most of them are a [[Man-in-the-Middle (MitM) attack]]). 

To prevent a downgrade attack, you must address its attack vector. If the vulnerability is due to support for export-grade ciphers, then the appropriate measure is to stop supporting such ciphers. If, on the other hand, the vulnerability is associated with support for previous versions of TLS or SSL, this needs to be addressed.

Implementing a [secure and stable TLS configuration](https://crashtest-security.com/enable-tls-encryption/) is one of the best measures you can take to address a host of causes that can lead to a downgrade attack. This includes providing support only to strong protocols such as TLS 1.2 and 1.3 (i.e., removing backward compatibility) and solid ciphers with no known downgrade vulnerabilities.

[Enabling the TLS_FALLBACK_SCSV signal](https://crashtest-security.com/enable-tls-fallback-scsv/) as part of your TLS configuration is another good step in preventing downgrade attacks. Suppose you do decide to support lower protocol versions. In that case, this will prevent your server from downgrading its protocol if the client can meet it at a higher version but is advertising a lower one (possibly due to man-in-the-middle interference).