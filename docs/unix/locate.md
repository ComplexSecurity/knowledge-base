icon:fontawesome/solid/terminal

# Locate

Used to quickly find filenames in a database that indexes the system's files and directories.

## Usage

```bash
locate [OPTION]... PATTERN...
```

## Flags

```bash
  -b, --basename         search only the file name portion of path names
  -c, --count            print number of matches instead of the matches
  -d, --database DBPATH  search for files in DBPATH
                         (default is /var/lib/plocate/plocate.db)
  -i, --ignore-case      search case-insensitively
  -l, --limit LIMIT      stop after LIMIT matches
  -0, --null             delimit matches by NUL instead of newline
  -N, --literal          do not quote filenames, even if printing to a tty
  -r, --regexp           interpret patterns as basic regexps (slow)
      --regex            interpret patterns as extended regexps (slow)
  -w, --wholename        search the entire path name (default; see -b)
      --help             print this help
      --version          print version information
```

## Examples

##### Update local database

```bash
sudo updatedb
```

##### Using locate to find python3 related items

```bash
$ locate python3 | head
/etc/python3
/etc/python3.10
/etc/python3.9
/etc/python3/debian_config
/etc/python3.10/sitecustomize.py
/etc/python3.9/sitecustomize.py
/usr/bin/dh_python3-ply
/usr/bin/ipython3
/usr/bin/pybabel-python3
/usr/bin/python3
```

## References

- [Linux.die.net - locate](https://linux.die.net/man/1/locate)
