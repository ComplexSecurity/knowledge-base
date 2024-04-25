The `grep` command in Unix and Unix-like operating systems is a powerful tool used for searching plain-text data for lines that match a given regular expression. Its name comes from the ed command `g/re/p` (globally search a [[Regular Expressions|regular expression]] and print). `grep` is widely used for searching in files, or combined with other commands in pipelines for various text-processing tasks.

Some basic examples include:

```bash
grep "search_string" filename.txt
```

This command will search for `search_string` in `filename.txt` and print lines where the string is found.

```bash
grep -i "search_string" filename.txt
```

The -i option makes the search case-insensitive.

```bash
grep -c "search_string" filename.txt
```

The -c option will count the number of lines that match the search string.

```bash
grep -n "search_string" filename.txt
```

The `-n` option prints the line number before each matching line.

```bash
grep -r "search_string" /path/to/directory
```

The -r option tells grep to recursively search all files in the specified directory and its subdirectories.

```bash
grep -v "search_string" filename.txt
```

The -v option inverts the match, showing only the lines that do not contain the search string.

```bash
grep "^[0-9]" filename.txt
```

This searches for lines in filename.txt that start with a number. grep supports regular expressions for more complex pattern matching.

```bash
grep -A 2 "search_string" filename.txt  # Show 2 lines after the match
grep -B 2 "search_string" filename.txt  # Show 2 lines before the match
grep -C 2 "search_string" filename.txt  # Show 2 lines before and after the match
```

This displays lines before and after the matches.

```bash
grep -e "string1" -e "string2" filename.txt
```

The -e option allows you to specify multiple search patterns.

```bash
cat filename.txt | grep "search_string"
```

Here, `grep` is used to filter the output of another command (`cat` in this case).
