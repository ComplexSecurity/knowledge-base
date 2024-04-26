In [PHP](../programming/php.md), the `data` wrapper is a type of stream wrapper that allows data to be read from or written to a string in the same way as you would with a file. This feature is particularly useful for manipulating data in string format using file handling functions, without the need to create a physical file on the file system.

The `data` wrapper is commonly used in scenarios where you want to treat a string as a stream resource, which enables you to use PHP's file system functions (like [fopen()](../programming/fopen.md), [fwrite()](../programming/fwrite.md), [fread()](../programming/fread.md), etc.) on data stored in a string.

A data URI using the data wrapper in PHP follows the format:

```php
data:[<mediatype>][;base64],<data>
```

- `<mediatype>` is the [MIME type](../misc/mime.md) of the data, like `text/plain` or `image/png`.
- `base64` is an optional parameter indicating that the data is base64-encoded.
- `<data>` is the actual data you want to encode in the URI.

An example of how you might use it:

```php
// Data URI containing plain text
$data = 'data:text/plain;base64,' . base64_encode('Hello, World!');

// Open a stream to the data URI
$stream = fopen($data, 'r');

// Read from the stream
$content = fread($stream, 1024);

// Close the stream
fclose($stream);

// Output the content
echo $content;  // Outputs: Hello, World!
```

!!! info
    A simple string 'Hello, World!' is [base64](../misc/base64.md)-encoded and used to create a data URI. This URI is then opened as a stream, and the content is read back from the stream.

The `data` wrapper itself in PHP is not inherently vulnerable; however, like any tool, its security depends on how it's used.

The `data` wrapper is a feature that allows data to be treated as a file or stream, which can be extremely useful, but certain use cases can introduce security risks if not handled properly.

If the data used in a `data` URI comes from an untrusted source, it must be properly validated and sanitized to avoid security risks such as [code injection](../security/cinj.md) or [cross-site scripting (XSS)](../web/xss.md). This is particularly important when handling [HTML](../web/html.md), [JavaScript](../programming/js.md), or other types of executable content.

The `data` wrapper is often used with base64 encoded data. While base64 encoding/decoding itself is not a security risk, it's essential to ensure that the decoded data is safe and expected, especially if it's dynamically generated or derived from user input.

Since the `data` wrapper allows data to be encoded directly in a URI, there's a potential risk of resource exhaustion if very large data strings are used. This can lead to performance degradation or crashing of the script or server.

When used in a web context (such as embedding images in HTML or [CSS](../programming/css.md)), it's important to ensure that the data URIs do not contain malicious content, especially when the content is dynamically generated based on user input or external sources.
