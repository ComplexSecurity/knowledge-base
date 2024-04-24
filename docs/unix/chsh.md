icon:fontawesome/solid/terminal

# Chsh

Command-line utility used to change a user's default login shell.

## Usage

```bash
chsh [options] [LOGIN]
```

## Flags

```bash
Options:
  -h, --help                    display this help message and exit
  -R, --root CHROOT_DIR         directory to chroot into
  -s, --shell SHELL             new login shell for the user account
```

## Examples

##### Change default shell

```bash
$ chsh -s /bin/zsh

Password:
Changing the login shell for <user>
```

## References

- [Linux.die.net](https://linux.die.net/man/1/chsh)
