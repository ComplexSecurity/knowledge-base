icon:fontawesome/solid/terminal

# Groupdel

Command-line utility used to delete a group from the system's group database.

## Usage

```bash
groupdel [options] GROUP
```

## Flags

```bash
Usage: groupdel [options] GROUP

Options:
  -h, --help                    display this help message and exit
  -R, --root CHROOT_DIR         directory to chroot into
  -f, --force                   delete group even if it is the primary group of a user
      --extrausers              Use the extra users database
```

## References

- [Linux.die.net](https://linux.die.net/man/8/groupdel)
