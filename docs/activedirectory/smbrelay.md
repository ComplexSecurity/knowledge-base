SMB Relay attacks are a type of network attack where an attacker intercepts and relays authentication requests from a client to another server. This attack exploits the [Server Message Block (SMB)](../protocols/smb.md) protocol, particularly its authentication mechanism, and is effective in networks where [SMB Signing](../activedirectory/smbsign.md) is not enforced.

The attacker positions themselves to intercept SMB authentication traffic, which often involves tricking a client into sending its authentication request to the attacker's machine. Instead of trying to decrypt or crack the authentication data, the attacker simply relays this request to another server or service on the network. If the target server accepts the relayed authentication (i.e., it trusts the client's machine), the attacker gains access to the target server with the same rights as the intercepted user.
a
Some popular tools for performing it include:

[Impacket](../tools/impacket.md) [ntlmrelayx](../tools/ntlmrelayx.md):

- A popular tool for performing [NTLM relay attacks](../security/ntlmattack.md) (which includes SMB relaying). An example usage may be:

```bash
python ntlmrelayx.py -t smb://<TARGET_IP> -smb2support
```

!!! info
    This command relays intercepted SMB authentication requests to the specified target IP address.

[Responder](../tools/responder.md):

- Often used in conjunction with ntlmrelayx, Responder can poison network traffic to intercept authentication requests. An example usage may be:

```bash
python Responder.py -I <INTERFACE> -wrf
```

!!! info
    This command runs Responder on a specified network interface, intercepting network traffic.



