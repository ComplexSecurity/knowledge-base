icon:fontawesome/solid/terminal

# Lsmod

Displays a list of currently loaded kernel modules, showing their status and dependencies.

## Usage

```bash
lsmod
```

## Examples

```bash
lsmod

Module                  Size  Used by
uas                    24576  0
usb_storage            77824  2 uas
nfnetlink              16384  0
ccm                    20480  6
hid_logitech_hidpp     40960  0
hid_logitech_dj        24576  0
thunderbolt           167936  0
pci_stub               16384  1
vboxpci                24576  0
vboxnetadp             28672  0
vboxnetflt             28672  0
vboxdrv               487424  3 vboxpci,vboxnetadp,vboxnetflt
[...]
```

## References

- [Linux.die.net](https://linux.die.net/man/8/lsmod)
