Impacket's `ntlmrelayx` is a powerful tool designed to perform [NTLM relay attacks](../activedirectory/relayatt.md). An NTLM relay attack is a type of security vulnerability where an attacker intercepts [NTLM](../security/ntlm.md) (NT LAN Manager) authentication traffic and then relays this traffic to another server to authenticate as the intercepted user. This tool is part of the [Impacket](../tools/impacket.md) suite, a collection of [Python](../programming/python.md) classes for working with network protocols.

The primary function of `ntlmrelayx` is to intercept and relay NTLM authentication requests from one host to another. This allows the attacker to authenticate to a target server with the credentials of a user whose traffic was intercepted. It can relay credentials to various types of services, including [SMB](../protocols/smb.md), [HTTP](../web/http.md), and others that support NTLM authentication.

`ntlmrelayx` can be configured to automatically execute specific actions upon successful relay, such as running commands, dumping hashes, or exploiting known vulnerabilities. Often used in conjunction with other Impacket tools like [responder](../tools/responder.md), which can poison network traffic and facilitate the capture of NTLM authentication messages for relay.

Here's an example:

```bash
python ntlmrelayx.py -t smb://<TARGET_IP>
```

- `-t smb://<TARGET_IP>` specifies the target to relay the NTLM authentication to, using SMB protocol.
- You would typically run this command alongside a tool like Impacket's `responder`, which induces network clients to send their NTLM authentication messages to you.

