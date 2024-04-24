icon:material/apple

# Ipconfig

Command-line tool on macOS used to configure and display network interface parameters and DNS settings.

## Usage

```bash
ipconfig <command> <args>
```

## Flags

```bash
where <command> is one of waitall, getifaddr, ifcount, getoption, getiflist, getsummary, getpacket, getv6packet, getra, set, setverbose
```

## Examples

##### Get list of interfaces

```bash
ipconfig getiflist
en4 en5 en6 en0 bridge0 en7
```

##### Get address of specific interface

```bash
ipconfig getifaddr en7
10.10.13.37
```
