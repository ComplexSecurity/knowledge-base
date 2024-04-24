icon:fontawesome/solid/terminal

# Lsb_release

Displays Linux Standard Base and distribution-specific information about the operating system.

## Usage

```bash
lsb_release [options]
```

## Flags

```bash
Options:
  -h, --help         show this help message and exit
  -v, --version      show LSB modules this system supports
  -i, --id           show distributor ID
  -d, --description  show description of this distribution
  -r, --release      show release number of this distribution
  -c, --codename     show code name of this distribution
  -a, --all          show all of the above information
  -s, --short        show requested information in short format
```

## Examples

##### Show distribution specific info

```bash
$ lsb_release -a

No LSB modules are available.
Distributor ID: Ubuntu
Description:    Ubuntu 18.04.4 LTS
Release:    18.04
Codename:   bionic
```

```bash
$ lsb_release -a

No LSB modules are available.
Distributor ID: Ubuntu
Description:    Ubuntu 20.04 LTS
Release:    20.04
Codename:   focal
```

## References

- [Linux.die.net](https://linux.die.net/man/1/lsb_release)
