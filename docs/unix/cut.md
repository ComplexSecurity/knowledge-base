icon:fontawesome/solid/terminal

# Cut

Command-line utility used to remove sections from each line of files, allowing users to extract text by specifying column positions.

## Usage

```bash
cut OPTION... [FILE]...
```

## Flags

```bash
Usage: cut OPTION... [FILE]...
Print selected parts of lines from each FILE to standard output.

With no FILE, or when FILE is -, read standard input.

Mandatory arguments to long options are mandatory for short options too.
-b, --bytes=LIST select only these bytes
-c, --characters=LIST select only these characters
-d, --delimiter=DELIM use DELIM instead of TAB for field delimiter
-f, --fields=LIST select only these fields; also print any line
that contains no delimiter character, unless
the -s option is specified
-n (ignored)
--complement complement the set of selected bytes, characters
or fields
-s, --only-delimited do not print lines not containing delimiters
--output-delimiter=STRING use STRING as the output delimiter
the default is to use the input delimiter
-z, --zero-terminated line delimiter is NUL, not newline
--help display this help and exit
--version output version information and exit

Use one, and only one of -b, -c or -f. Each LIST is made up of one
range, or many ranges separated by commas. Selected input is written
in the same order that it is read, and is written exactly once.
Each range is one of:

N N'th byte, character or field, counted from 1
N- from N'th byte, character or field, to end of line
N-M from N'th to M'th (included) byte, character or field
-M from first to M'th (included) byte, character or field

GNU coreutils online help: <https://www.gnu.org/software/coreutils/>
Full documentation at: <https://www.gnu.org/software/coreutils/cut>
or available locally via: info '(coreutils) cut invocation'
```

## Examples

##### Cut one or specific bytes

```bash
cut -b 1 <file>
cut -b 1,2,3 <file>
```

##### Cut list of bytes

```bash
cut -b 1-3,5-7 <file>
```

##### Cut by fields

```bash
cut -f 1 <file>
cut -f 2-4 <file>
```

##### Cut range of fields

```bash
cut -f 1-2,4-5 <file>
```

##### Cut by delimiter

```bash
cut -d '<delimiter>' -f <field> <file>
```

##### Cut by delimiter with output delimiter

```bash
cut -d '<delimiter>' -f <field> --output-delimiter='<output-delimiter>' <file>

E.g. with tab after each field
cut -d '<delimter>' -f <field> --output-delimiter=$'\t' <file>
```

## References

- [GNU.org](https://www.gnu.org/software/coreutils/cut)
