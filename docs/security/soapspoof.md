SOAPAction Spoofing is a type of attack against web services that use the [SOAP|Simple Object Access Protocol (SOAP)](). This attack involves manipulating or forging the `SOAPAction` header in a SOAP request to trick the server into performing an unintended action. The `SOAPAction` header in a SOAP request is supposed to indicate the specific action or operation that the request is intended to trigger. By spoofing this header, an attacker can potentially bypass security checks or access unauthorized functionality.

The attacker modifies the `SOAPAction` header in the SOAP request to an unexpected value or to an action that they are not authorized to use. If the web service does not properly validate the `SOAPAction` header or relies solely on it for routing requests to the appropriate handlers, this manipulation can allow the attacker to access functions they shouldn't have access to.

The spoofing might exploit logical flaws in the web service where certain actions are inadequately protected or where the routing of requests is based solely on the `SOAPAction` header.

Imagine a web service that offers two operations: `getUserDetails` (which is intended to be publicly accessible) and `deleteUser` (which is restricted to administrators). These operations might be invoked using SOAP requests with `SOAPAction` headers like:

- `SOAPAction: "http://example.com/getUserDetails"`
- `SOAPAction: "http://example.com/deleteUser"`

An attacker might normally only have access to `getUserDetails`. However, if the web service inadequately checks the user's permissions and relies solely on the `SOAPAction` header to route the request, the attacker could modify their SOAP request to:

```http
SOAPAction: "http://example.com/deleteUser"
```

!!! info
    Even though they are not an administrator, if the service does not verify their authorization for the `deleteUser` action, it might process this request, allowing the attacker to delete users.

