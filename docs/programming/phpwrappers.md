PHP wrappers are a powerful feature in [PHP](../programming/php.md) used to access various types of data streams through a common interface. These wrappers allow PHP to interact with different types of data using the same set of functions you would use with regular files

The types of wrappers in PHP include:

1. File System Wrappers: This is the default wrapper that deals with file system functions. It allows access to local file systems. For example, when you use [fopen()](../programming/fopen.md) or [file_get_contents()](../programming/fgc.md) for files, you're using this wrapper.
2. [HTTP](../web/http.md) and [HTTPS](../web/https.md) Wrappers: They allow PHP to access data over HTTP/HTTPS. For example, you can read a web page or an online file using `file_get_contents('http://example.com')`.
3. [FTP](../protocols/ftp.md) and [FTPS](../protocols/ftps.md) Wrappers: These are used for accessing files over FTP/FTPS. You can open, read, or write files on a remote FTP server.
4. PHP Input/Output Wrappers:
	- `php://input` allows you to read raw data from the request body.
	- `php://output` is a write-only stream that allows you to write to the output buffer.
	- `php://memory` and `php://temp` are used for storing data in memory or in a temporary file, respectively.
5. Compression Wrappers (zlib): This wrapper allows access to compressed files. For instance, `compress.zlib://file.gz` lets you read and write to gzipped files transparently.
6. Data Wrapper: It is used to read data in a string as if it were a regular file. It's useful for encoding data in [base64](../misc/base64.md) or [URL encoding](../web/urlenc.md).
7. Glob Wrapper: Used with functions like `glob()` to match file patterns.
8. SSH2 Wrapper: For accessing remote resources via the [Secure Shell](../protocols/ssh.md) 2 protocol.
9. Custom Stream Wrappers: PHP allows developers to define their own protocol wrappers, enabling the creation of custom stream handling logic.

Some example uses include reading from a website:

```php
$content = file_get_contents('http://example.com');
echo $content;
```

Or writing to a compressed file:

```php
$fp = fopen('compress.zlib://file.gz', 'w');
fwrite($fp, 'data to compress');
fclose($fp);
```

Or reading JSON from PHP input:

```php
$json = file_get_contents('php://input');
$data = json_decode($json);
```




