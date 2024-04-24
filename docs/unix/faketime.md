icon:fontawesome/solid/terminal

# Faketime

Command-line utility that allows users to run programs with a modified system time without changing the actual system clock.

## Installation

```bash
sudo apt install faketime
```

## Usage

```bash
faketime [OPTIONS]
```

## Flags

```bash
       --help show usage information and quit.

       --version
              show version information and quit.

       -m     use the multi-threading variant of libfaketime.

       -f     use the advanced timestamp specification format.
```

## Examples

```bash
$ date
Fri 28 Jan 2022 11:19:20 AM EST

$ faketime -f +4h date
Fri 28 Jan 2022 03:19:20 PM EST

$ faketime -f -4h bash
$ date
Fri 28 Jan 2022 07:19:20 AM EST
```

## References

- [Manpages.ubuntu.com - Faketime](https://manpages.ubuntu.com/manpages/trusty/man1/faketime.1.html)
