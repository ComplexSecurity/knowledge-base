Basic authentication is a simple authentication scheme built into the HTTP protocol. The client sends HTTP requests with the Authorization [[HTTP Headers|header]] that contains the word Basic word followed by a space and a base64-encoded string username:password. 

For example, to authorize as demo:p@55w0rd the client would send:

```bash
Authorization: Basic ZGVtbzpwQDU1dzByZA==
```

!!! warning
    Because base64 is easily decoded, Basic authentication should only be used together with other security mechanisms such as HTTPS/SSL.

