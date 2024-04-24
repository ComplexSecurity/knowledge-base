icon:fontawesome/solid/terminal

# Cat

Command-line utility used to display the contents of files, concatenate files, and redirect output in the terminal.

## Usage

```bash
cat [OPTION]... [FILE]...
```

## Flags

```bash
-A, --show-all
    equivalent to -vET
-b, --number-nonblank
    number nonempty output lines
-e
    equivalent to -vE
-E, --show-ends
    display $ at end of each line
-n, --number
    number all output lines
-s, --squeeze-blank
    suppress repeated empty output lines
-t
    equivalent to -vT
-T, --show-tabs
    display TAB characters as ^I
-u
    (ignored)
-v, --show-nonprinting
    use ^ and M- notation, except for LFD and TAB
--help
    display this help and exit
--version
    output version information and exit
```

## Examples

```bash
cat file1.txt
F1@9_NoWyoUArE63t7in97H3r3413
```

## References

- [Linux.die.net](https://linux.die.net/man/1/cat)
