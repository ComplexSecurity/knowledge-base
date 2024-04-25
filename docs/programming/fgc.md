The `file_get_contents()` function in [[PHP]] is a simple and convenient way to read the entire contents of a file into a string. It's widely used due to its ease of use and efficiency for reading files, especially when dealing with text files or the contents of a URL.

It can be used to read local files from the file system. The function reads the entire file and returns its contents as a string. If the PHP configuration allows, `file_get_contents()` can also be used to read content from a URL, effectively fetching data from the web.

It supports the use of a context resource created with `stream_context_create()` to modify the behavior of the request (like setting [[HTTP headers]] when fetching a URL).  If the function fails to read a file (e.g., due to permissions issues or the file not existing), it returns `FALSE`.

The syntax is:

```php
$content = file_get_contents(string $filename, bool $use_include_path = false, resource $context = null, int $offset = 0, int $length = null): string|false
```

- `$filename`: Path to the file or URL.
- `$use_include_path`: Whether to search for the file in the include_path (optional).
- `$context`: A context resource created with `stream_context_create()` to specify options like headers, proxy settings, etc. (optional).
- `$offset`: Offset where reading starts on the original stream (optional).
- `$length`: Maximum length of data read (optional).

Some examples include reading a local file:

```php
$content = file_get_contents('/path/to/file.txt');
echo $content;
```

And reading from a URL:

```php
$content = file_get_contents('http://example.com');
echo $content;
```

When using `file_get_contents()` with user-provided data (e.g., file paths or URLs), it's crucial to validate and sanitize the input to prevent security vulnerabilities, such as [[Local File Inclusion]] (LFI) or [[Remote File Inclusion]] (RFI). Additionally, when reading from external URLs, be aware of the risks of fetching untrusted content, which could include malicious data or code.

An example of vulnerable code is:

```php
<?php
// A vulnerable script where the file name is taken from user input
$filePath = $_GET['file'];

// Using file_get_contents() with user-controlled input
$content = file_get_contents($filePath);

echo $content;
?>
```

>[!caution]
>In this example, an attacker could manipulate the query string in the URL to access sensitive files. For instance:

```bash
http://example.com/script.php?file=../../etc/passwd
```

This URL attempts to access the Unix/Linux system file `/etc/passwd`, which contains user information and could be sensitive.

