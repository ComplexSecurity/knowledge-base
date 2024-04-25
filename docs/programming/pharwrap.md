The `phar://` wrapper in [[PHP]] is a stream wrapper that allows PHP's file handling functions to interact with [[PHP Archive (PHAR)]] files. PHAR is a format used for packaging a complete PHP application or library into a single file. This format is similar to [[Java Archive (JAR)|JAR]] in [[Java]] and enables easy distribution and installation of PHP applications.

The `phar://` wrapper allows direct access to the files contained within a PHAR archive, similar to accessing files in a file system. PHP scripts can read from and write to files inside a PHAR archive using standard file functions, provided that the PHAR is not read-only.

PHAR files can be executed directly by the PHP interpreter, making them useful for distributing complete applications. PHAR archives encapsulate PHP code and resources, providing an isolated environment that reduces conflicts between different applications or libraries.

A usage example may be:

```php
// Reading a file from a PHAR archive
$file = fopen('phar://myapp.phar/internal/path/to/file.php', 'r');
$content = fread($file, filesize('phar://myapp.phar/internal/path/to/file.php'));
fclose($file);
echo $content;
```

>[!info]
>A file within a PHAR archive (`myapp.phar`) is being accessed, read, and its content is displayed. The internal path (`internal/path/to/file.php`) refers to the file's location within the PHAR archive.

PHAR files can contain executable PHP code, so there are security implications to consider:

- **Disabling PHAR Execution**: In some security-sensitive environments, executing PHAR files is disabled to prevent potential exploitation of vulnerabilities in the PHAR handling code.
- **User Uploads**: If a PHP application allows users to upload PHAR files, it should implement rigorous validation and sanitation to prevent code injection attacks.

PHAR files are particularly useful for distributing PHP libraries or applications as single files, simplifying deployment and usage. They are commonly used for command-line tools and applications that need to be easily portable without complex installation processes.