icon:fontawesome/solid/terminal

# Script

Captures and saves all terminal activity into a specified file, creating a typescript of the session.

## Usage

```bash
script [options] [file]
```

## Flags

```bash
Options:
 -a, --append                  append the output
 -c, --command <command>       run command rather than interactive shell
 -e, --return                  return exit code of the child process
 -f, --flush                   run flush after each write
     --force                   use output file even when it is a link
 -o, --output-limit <size>     terminate if output files exceed size
 -q, --quiet                   be quiet
 -t[<file>], --timing[=<file>] output timing data to stderr or to FILE
 -h, --help                    display this help
 -V, --version                 display version

For more details see script(1).
```

## Examples

##### Start terminal logging to file

```bash
script logfile.txt
```

## References

- [Linux.die.net](https://linux.die.net/man/1/script)
