icon:fontawesome/solid/terminal

# Mkdir

Used to create new directories.

## Usage

```bash
mkdir [OPTION] directory
```

## Examples

##### Create two separate directories

```bash
$ mkdir one two

$ ls
one two
```

##### Create directories in a directory

```bash
$ mkdir -p test/{one,two,three}

$ ls
test

$ ls test
one   three two
```

## References

- [Linux.die.net - mkdir](https://linux.die.net/man/1/mkdir)
