preg_replace() is a function in [[PHP]] used for performing a regular expression search and replace. It is part of PHP's PCRE (Perl Compatible Regular Expressions) functions and is widely used for finding and replacing patterns in strings.

The syntax is:

```php
preg_replace(pattern, replacement, subject, limit, count)
```

- **pattern**: The regular expression pattern to search for. It can be a string or an array of strings.
- **replacement**: The string or an array of strings to replace with.
- **subject**: The string or an array of strings to search and replace.
- **limit** (optional): The maximum possible replacements for each pattern in each subject string. If omitted, it defaults to -1 (no limit).
- **count** (optional): If specified, this variable will be filled with the number of replacements done.

The function uses Perl-compatible regular expressions and offers powerful pattern matching capabilities. You can use any valid PCRE [[Regular Expressions|regex]] pattern. preg_replace() searches for the specified pattern in the subject string(s) and replaces them with the replacement string.

An example may be:

```php
$string = "The quick brown fox jumps over the lazy dog.";
$pattern = "/quick/";
$replacement = "slow";
echo preg_replace($pattern, $replacement, $string);
// Outputs: The slow brown fox jumps over the lazy dog.
```

Both the subject and the pattern can be arrays. When provided as arrays, preg_replace() performs a search and replace on each element of the subject array. In the replacement string, you can use backreferences like $1, $2, etc., to refer to capturing groups defined in the pattern.

Common uses of preg_replace() include formatting strings, [[Input Sanitization|sanitizing input]], rewriting URLs, etc. Be cautious when using preg_replace() with user-supplied input as part of the pattern or replacement, as this can lead to complex security vulnerabilities, particularly if the /e modifier is used, which evaluates the replacement string as PHP code.



