icon:fontawesome/solid/terminal

icon:fontawesome/solid/terminal

# Ftp

Command-line client used to transfer files to and from a remote network site using the File Transfer Protocol.

## Installation

```bash
sudo apt install ftp
```

## Usage

```bash
ftp [OPTIONS] [hostname]
```

## Flags

```bash
Usage: { ftp | pftp } [-46pinegvtd] [hostname]
   -4: use IPv4 addresses only
   -6: use IPv6, nothing else
   -p: enable passive mode (default for pftp)
   -i: turn off prompting during mget
   -n: inhibit auto-login
   -e: disable readline support, if present
   -g: disable filename globbing
   -v: verbose mode
   -t: enable packet tracing [nonfunctional]
   -d: enable debugging
```

## Examples

##### Connect to FTP server

```bash
$ ftp <target>

Connected to <target>
220-FileZilla Server 0.9.60 beta
220-written by Tim Kosse (tim.kosse@filezilla-project.org)
220 Please visit https://filezilla-project.org/
Name (<target>):
```

##### Download a file

```bash
ftp> get Confidential.txt

local: Confidential.txt remote: Confidential.txt
200 PORT command successful.
125 Data connection already open; Transfer starting.
226 Transfer complete.
174 bytes received in 0.02 secs (9.1607 kB/s)
```

##### Upload a file

```bash
ftp> put Confidential.txt

local: Confidential.txt remote: Confidential.txt
200 PORT command successful.
125 Data connection already open; Transfer starting.
226 Transfer complete.
174 bytes received in 0.02 secs (9.1607 kB/s)
```

##### Get all files of specific extension

```bash
ftp> mget *.txt

mget Notes to do.txt?
200 PORT command successful.
125 Data connection already open; Transfer starting.
226 Transfer complete.
186 bytes received in 0.02 secs (10.9481 kB/s)
```

## References

- [Linux.die.net]https://linux.die.net/man/1/ftp)
