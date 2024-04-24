icon:fontawesome/solid/terminal

# Netplan

Configuration utility in Linux that uses YAML-based syntax to set up and manage network interfaces in a simple and consistent manner.

## Usage

```bash
usage: /usr/sbin/netplan  [-h] [--debug]  ...
```

## Flags

```bash
usage: /usr/sbin/netplan  [-h] [--debug]  ...

Network configuration in YAML

optional arguments:
  -h, --help  show this help message and exit
  --debug     Enable debug messages

Available commands:

    help      Show this help message
    apply     Apply current netplan config to running system
    generate  Generate backend specific configuration files from
              /etc/netplan/*.yaml
    info      Show current netplan version and available features
    ip        Retrieve IP information from the system
    try       Try to apply a new netplan config to running system, with
              automatic rollback
```

## Examples

##### Example config static IP

```bash
network:
    version: 2
    ethernets:
        enp3s0:
            addresses:
            - 10.20.30.10/24
            gateway4: 10.20.30.1
            nameservers:
                addresses:
                - 1.1.1.1
                - 9.9.9.9
```

##### DHCP

```bash
network:
  version: 2
  renderer: networkd
  ethernets:
    enp3s0:
      dhcp4: true
```

## References

- [Netplan.io](https://netplan.io/)
- [Netplan.io Examples](https://netplan.io/examples)
