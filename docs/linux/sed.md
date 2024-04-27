`sed`, short for "stream editor," is a powerful text-processing utility in Unix and Unix-like operating systems, including Linux and macOS. It's used primarily for parsing and transforming text data, such as extracting, replacing, and modifying strings or file content. 

`sed` is non-interactive, meaning it processes text without requiring user intervention, making it well-suited for scripting and batch processing.

`sed` reads input line by line, processes it according to provided commands, and outputs the result. It's particularly efficient for handling large text files. It uses [regular expressions](../security/regex.md) for pattern matching, which allows for complex text manipulations.

It is capable of editing files in-place (with the `-i` option), modifying the original file with the changes. It is commonly used for its search and replace functionality, which allows for the substitution of text patterns. `sed` commands can be scripted, enabling complex text transformations in shell scripts.

Some common uses for sed include:

- Text Replacement: Replacing words or patterns in a file. For example, to replace "cat" with "dog" in a file:

```bash
sed 's/cat/dog/' filename.txt
```

- Data Extraction and Reporting: Extracting specific data from text files, such as logs or configuration files.
- File Formatting and Text Conversions: Modifying the format of text data, like converting dates or removing whitespace.
- Automating Text Edits in Scripts: Using within shell scripts or in combination with other Unix tools for batch processing.

A simple example of Sed may be:

```bas
sed 's/foo/bar/g' input.txt > output.txt
```

This command replaces every occurrence of "foo" with "bar" in input.txt and writes the result to output.txt. The s stands for substitute, and the g at the end signifies a global replacement (replace all occurrences, not just the first one).

