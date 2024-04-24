icon:material/web

# Headers & Files

## Interesting Headers

#### Host Header Issues / WAF Bypass

```bash
curl -i -s -k -X $'GET' -H $'Host: example.com' $'http://<target>/'
```

```bash
Host header: www.xxx:80@xxx.burpcollaborator.net
Host header: evildomain.com
X-Forwarded-Host: evildomain.com > in request, if present in response then issue
X-Forwarded-Host: burpcollaborator
X-Forwarded-Host: http://burpcollaborator

X-Forwarded-For: 127.0.0.1
X-Forwarded-For: burpcollaborator
X-Forwarded-For: http://burpcollaborator

X-Custom-IP-Authorization: 127.0.0.1

X-Forwarded-Host
X-Forwarded-Port
X-Forwarded-Scheme
Origin: null
Origin: [siteDomain].attacker.com
X-Frame-Options: Allow
X-Forwarded-For: 127.0.0.1
X-Client-IP: 127.0.0.1
Client-IP: 127.0.0.1

X-Originating-IP: 127.0.0.1
X-Forwarded-For: 127.0.0.1
X-Remote-IP: 127.0.0.1
X-Remote-Addr: 127.0.0.1
X-Client-IP: 127.0.0.1
X-Host: 127.0.0.1
X-Forwared-Host: 127.0.0.1
X-Originating-IP:127.0.0.4
X-Forwarded-For:127.0.0.4
X-Remote-IP:127.0.0.4
X-Remote-Addr:127.0.0.4
```

## Basic NTLM Auth Header

```bash
Authorization: NTLM TlRMTVNTUAABAAAAB4IIAAAAAAAAAAAAAAAAAAAAAAA=
```

Or you can use Nmap:

```bash
nmap --script http-ntlm-info <target>
```

## Basic authentication test field

- [Basic auth generator](https://www.blitter.se/utils/basic-authentication-header-generator/)

| Username | Password   | Basic auth header                             |
| -------- | ---------- | --------------------------------------------- |
| admin    | admin      | Authorization: Basic YWRtaW46YWRtaW4=         |
| Aladdin  | OpenSesame | Authorization: Basic QWxhZGRpbjpPcGVuU2VzYW1l |
| test     | test       | Authorization: Basic dGVzdDp0ZXN0             |
| admin    | welcome    | Authorization: Basic YWRtaW46d2VsY29tZQ==     |
| guest    | welcome    | Authorization: Basic Z3Vlc3Q6d2VsY29tZQ==     |
| welkom   | welkom     | Authorization: Basic Z2FzdDp3ZWxrb20=         |

```bash
YWRtaW46YWRtaW4=
QWxhZGRpbjpPcGVuU2VzYW1l
dGVzdDp0ZXN0
YWRtaW46d2VsY29tZQ==
Z3Vlc3Q6d2VsY29tZQ==
Z2FzdDp3ZWxrb20=
```

## Potential IP Disclosure due to http1.0

```bash
curl --http1.0 -i -s -k -X $'GET' -H $'Host: ' $'http://<ip>/'
```

```bash
curl --http1.0 -i -s -k -X $'GET' -H $'Host: ' $'http://<dns>/'
```

## Interesting Files

#### Simple things

```bash
robots.txt
web.config
.git
trace.axd (IIS .NET ASPNET)
.well-known/openid-configuration
```

#### Umbraco

- [wordlist_umbraco.txt](../assets/files/wordlist_umbraco.txt){:download="wordlist_umbraco.txt"}

```bash
/Umbraco
/Umbraco/Views/install/database.html
/Umbraco/Views/install/user.html
/Umbraco/Views/common/dialogs/login.html
/Umbraco/Webservices/publication.asmx
/Umbraco/Webservices/CheckForUpgrade.asmx
/Umbraco/Webservices/CMSNode.asmx
/Umbraco/Webservices/legacyAjaxCalls.asmx
/Umbraco/Webservices/progressStatus.asmx
```

#### Sharepoint

```bash
_vti_bin/Webs.asmx
_vti_bin/SPDisco.aspx
_vti_inf.html (http://www.ktskumar.com/2015/09/remote-identification-of-sharepoint-version/)
_vti_pvt/service.cnf (http://www.ktskumar.com/2015/09/remote-identification-of-sharepoint-version/)
```

#### ADFS

```bash
/adfs/ls
/adfs/ls/IdpInitiatedSignOn.aspx?
```

#### Microsoft Remote Gateway (RDG / RDGateway)

```bash
https://<domain>/RDWeb/Pages/en-US/login.aspx?ReturnUrl=/RDWeb/Pages/en-US/Default.aspx
https://<domain>/RDWeb/Pages/en-US/password.aspx
```

#### Topdesk Admin Page

Try header if blocked

```bash
<domain>/tas/admin/index.jsp
```

```bash
X-Forwarded-For: 127.0.0.1
```

#### Oracle APEX

- [Hacking-Oracle-APEX.pdf](../assets/files/Hacking-Oracle-APEX.pdf){:download="Hacking-Oracle-APEX.pdf"}

```bash
python3 sqlmap.py -u "https://<url>/apex/wwv_flow.show?p_flow_id=121&p_flow_step_id=1&p_instance=0&p_arg_name=P1_ITEM&p_arg_value=ABC" --batch --dbms Oracle -p p_arg_value --flush-session
```

Oracle Application Express management interface

```bash
<url>/apex/gexswe
```

#### JBOSS

```bash
:8080/invoker/EJBInvokerServlet
:8080/invoker/JMXInvokerServlet
:8080/jmx-console
:8080/web-console
:8080/admin-console [with credentials admin:admin]
:8080/jbpm-console
```

#### Apache TomCat

```bash
:8080/manager/html [with credentials admin:blank]
```
