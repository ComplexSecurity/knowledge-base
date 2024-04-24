icon:fontawesome/solid/terminal

# Awk

Powerful text processing programming language used for pattern scanning and processing.

## Usage

```bash
awk <OPTIONS> <PROGRAM> <FILE>
```

## Flags

```bash
OFS=""                      Add seperator between ""
$NF                         End of file
'BEGIN {print "SomeText"}'  Start with text
```

## Examples

##### Pipe to awk and print the first and third object in a line

```bash
who | awk '{print $1,$3}'
```

##### Cat a file and print first, second and last word of the file

```bash
cat <file> | awk '{print $1,$2,$NF}'
```

##### Grab date, month and year

```bash
date | awk '{print $2,$3,$4}'
Result: 15 apr 2024
```

##### Use a file with separator ":" in items

```bash
awk -F: '{print $1,$6}' /etc/passwd
```

##### Grab first and last word per line in file

```bash
$ cat testfile.txt
This is a test file.
Or not this kind of test file.
Where are the cats.

$ cat testfile.txt | awk '{print $1,$NF}'
This file.
Or file.
Where cats.
```

## References

- [Linux.die.net](https://linux.die.net/man/1/awk)
