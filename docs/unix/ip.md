icon:fontawesome/solid/terminal

# Ip

## Usage

```bash
Usage: ip [ OPTIONS ] OBJECT { COMMAND | help }
       ip [ -force ] -batch filename
where  OBJECT := { link | address | addrlabel | route | rule | neigh | ntable |
                   tunnel | tuntap | maddress | mroute | mrule | monitor | xfrm |
                   netns | l2tp | fou | macsec | tcp_metrics | token | netconf | ila |
                   vrf | sr | nexthop }
```

## Flags

```bash
OPTIONS := { -V[ersion] | -s[tatistics] | -d[etails] | -r[esolve] |
            -h[uman-readable] | -iec | -j[son] | -p[retty] |
            -f[amily] { inet | inet6 | mpls | bridge | link } |
            -4 | -6 | -I | -D | -M | -B | -0 |
            -l[oops] { maximum-addr-flush-attempts } | -br[ief] |
            -o[neline] | -t[imestamp] | -ts[hort] | -b[atch] [filename] |
            -rc[vbuf] [size] | -n[etns] name | -N[umeric] | -a[ll] |
            -c[olor]}
```

| Object    | Abbreviated form | Purpose                                            |
| --------- | ---------------- | -------------------------------------------------- |
| link      | l                | Network device                                     |
| address   | a/addr           | Protocol (IP or IPv6) address on a device          |
| addrlabel | addrl            | Label configuration for protocol address selection |
| neighbour | n/neigh          | ARP or NDISC cache entry                           |
| route     | r                | Routing table entry                                |
| rule      | ru               | Rule in routing policy database                    |
| maddress  | m/maddr          | Multicast address                                  |
| mroute    | mr               | Multicast routing cache entry                      |
| tunnel    | t                | Tunnel over IP                                     |
| xfrm      | x                | Framework for IPsec protocol                       |

## Examples

##### Show IPv4 addresses

```bash
$ ip -4 a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state UP group default qlen 1000
    inet 10.10.30.253/24 brd 10.10.30.255 scope global eth0
       valid_lft forever preferred_lft forever
```

##### Show IPv6 addresses

```bash
$ ip -6 addr

1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 state UNKNOWN qlen 1000
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
3: wlp4s0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 state UP qlen 1000
    inet6 fe80::67c3:63c4:a12e:7f2a/64 scope link noprefixroute
       valid_lft forever preferred_lft forever
```

##### Show routing tables

```bash
$ ip r list
default via 10.10.30.254 dev eth0 proto static
10.10.30.0/24 dev eth0 proto kernel scope link src 10.10.30.253
```

## References

- [Linux.die.net](https://linux.die.net/man/8/ip)
- [HowToGeek.com](https://www.howtogeek.com/657911/how-to-use-the-ip-command-on-linux/)
- [Cyberciti.biz - Linux ip Command Examples](https://www.cyberciti.biz/faq/linux-ip-command-examples-usage-syntax)
