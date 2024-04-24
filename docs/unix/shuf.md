icon:fontawesome/solid/terminal

# Shuf

Command-line utility used for shuffling or randomizing input lines.

## Installation

```bash
sudo apt install shuf
```

## Usage

```bash
shuf [OPTION]... [FILE]
  or:  shuf -e [OPTION]... [ARG]...
  or:  shuf -i LO-HI [OPTION]...
```

## Flags

```bash
With no FILE, or when FILE is -, read standard input.

Mandatory arguments to long options are mandatory for short options too.
  -e, --echo                treat each ARG as an input line
  -i, --input-range=LO-HI   treat each number LO through HI as an input line
  -n, --head-count=COUNT    output at most COUNT lines
  -o, --output=FILE         write result to FILE instead of standard output
      --random-source=FILE  get random bytes from FILE
  -r, --repeat              output lines can be repeated
  -z, --zero-terminated     line delimiter is NUL, not newline
      --help     display this help and exit
      --version  output version information and exit

GNU coreutils online help: <https://www.gnu.org/software/coreutils/>
Report any translation bugs to <https://translationproject.org/team/>
Full documentation <https://www.gnu.org/software/coreutils/shuf>
or available locally via: info '(coreutils) shuf invocation'
```

## Examples

- passwords contains 5264448 passwords

```bash
$ shuf -n 5 passwords
November2020,
LaPalma2023!
Christ1@1
Zaq.xsw23
Willies011
```

## References

- [Linux.die.net - Shuf](https://linux.die.net/man/1/shuf)
