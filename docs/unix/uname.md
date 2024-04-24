icon:fontawesome/solid/terminal

# Uname

Command-line utility used to display system information such as kernel version, machine hardware name, and operating system.

## Usage

```bash
uname [OPTION]...
```

## Flags

```bash
With no OPTION, same as -s.

  -a, --all                print all information, in the following order,
                             except omit -p and -i if unknown:
  -s, --kernel-name        print the kernel name
  -n, --nodename           print the network node hostname
  -r, --kernel-release     print the kernel release
  -v, --kernel-version     print the kernel version
  -m, --machine            print the machine hardware name
  -p, --processor          print the processor type (non-portable)
  -i, --hardware-platform  print the hardware platform (non-portable)
  -o, --operating-system   print the operating system
      --help     display this help and exit
      --version  output version information and exit

GNU coreutils online help: <https://www.gnu.org/software/coreutils/>
Full documentation at: <https://www.gnu.org/software/coreutils/uname>
or available locally via: info '(coreutils) uname invocation'
```

## Examples

```bash
$ uname -a
Linux testsystem 5.8.0-7642-generic #47~1614007149~20.04~82fb226-Ubuntu SMP Tue Feb 23 02:56:27 UTC  x86_64 x86_64 x86_64 GNU/Linux
```

## References

- []()
