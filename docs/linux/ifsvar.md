# $IFS Environment Varable

The \$IFS environment variable in Linux stands for "Internal Field Separator". It is used by the shell to determine how to do word splitting, i.e., how to recognize word boundaries. In essence, $IFS defines a string of characters that the shell treats as delimiters between words or fields.

By default, `$IFS` contains three characters: **space**, **tab**, and **newline**. This means that in its default state, the shell will split words or fields on spaces, tabs, and newlines. You can change the value of `$IFS` to alter the behavior of shell scripts or commands. For instance, if you set `IFS=,`, the shell will treat commas as the delimiter for splitting words.

It's commonly used in shell scripts and command lines, especially when reading data from a file or processing input strings. For example, when parsing CSV files, setting `IFS` to a comma is useful. Modifying `$IFS` can significantly change the behavior of scripts and commands. It should be done cautiously, and typically, `IFS` is restored to its original state after its custom use in a script.

Changes to `IFS` in a subshell do not affect the parent shell. So, scripts often modify `IFS` in a subshell to avoid side effects. It's also used in command-line arguments and in parsing file paths, where directories and filenames are separated by specific delimiters (like `/` in file paths).