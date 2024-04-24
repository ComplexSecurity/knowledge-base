icon:fontawesome/solid/terminal

# Delv

Command-line tool used for DNS lookup and debugging, providing detailed answers about DNS queries and validations.

## Usage

```bash
delv [@server] {q-opt} {d-opt} [domain] [q-type] [q-class]
```

## Flags

```bash
Usage:  delv [@server] {q-opt} {d-opt} [domain] [q-type] [q-class]
Where:  domain    is in the Domain Name System
        q-class  is one of (in,hs,ch,...) [default: in]
        q-type   is one of (a,any,mx,ns,soa,hinfo,axfr,txt,...) [default:a]
        q-opt    is one of:
                 -x dot-notation     (shortcut for reverse lookups)
                 -d level            (set debugging level)
                 -a anchor-file      (specify root and dlv trust anchors)
                 -b address[#port]   (bind to source address/port)
                 -p port             (specify port number)
                 -q name             (specify query name)
                 -t type             (specify query type)
                 -c class            (option included for compatibility;
                                      only IN is supported)
                 -4                  (use IPv4 query transport only)
                 -6                  (use IPv6 query transport only)
                 -i                  (disable DNSSEC validation)
                 -m                  (enable memory usage debugging)
        d-opt    is of the form +keyword[=value], where keyword is:
                 +[no]all            (Set or clear all display flags)
                 +[no]class          (Control display of class)
                 +[no]crypto         (Control display of cryptographic
                                      fields in records)
                 +[no]multiline      (Print records in an expanded format)
                 +[no]comments       (Control display of comment lines)
                 +[no]rrcomments     (Control display of per-record comments)
                 +[no]unknownformat  (Print RDATA in RFC 3597 "unknown" format)
                 +[no]short          (Short form answer)
                 +[no]split=##       (Split hex/base64 fields into chunks)
                 +[no]tcp            (TCP mode)
                 +[no]ttl            (Control display of ttls in records)
                 +[no]trust          (Control display of trust level)
                 +[no]rtrace         (Trace resolver fetches)
                 +[no]mtrace         (Trace messages received)
                 +[no]vtrace         (Trace validation process)
                 +[no]dlv            (DNSSEC lookaside validation anchor)
                 +[no]root           (DNSSEC validation trust anchor)
                 +[no]dnssec         (Display DNSSEC records)
        -h                           (print help and exit)
        -v                           (print version and exit)
```

## Examples

##### DNSSEC enabled

```bash
$ delv @1.1.1.1 cloudflare.com

; fully validated
cloudflare.com.     217 IN  A   104.17.175.85
cloudflare.com.     217 IN  A   104.17.176.85
cloudflare.com.     217 IN  RRSIG   A 13 2 300 20200314153130 20200312133130 34505 cloudflare.com. obmtyacO2462qIC97UGdcd8EYc7/Bl2kqbG281oZO1yVWKV//jWav5ET 1p9IjL6anF8Kq4Puvf9DSQ1SjvaRGw==
```

##### DNSSEC disabled

```bash
$ delv @1.1.1.1 google.com

; unsigned answer
google.com.     3200171710 IN   A   172.217.17.46
```

## References

- [Ubuntun Man Pages](https://manpages.ubuntu.com/manpages/jammy/en/man1/delv.1.html#:~:text=delv%20sends%20to%20a%20specified,of%20trust%20for%20DNSSEC%20validation.)
