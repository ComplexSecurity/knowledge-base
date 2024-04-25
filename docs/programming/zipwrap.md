The ZIP PHP wrapper is a feature in [[PHP]] that allows for the manipulation of ZIP archives using the standard file handling functions. It provides a way to read from and write to ZIP files directly through the PHP's file stream interface, as if they were regular file systems. This feature simplifies the process of working with ZIP files in PHP scripts.

It allows developers to use familiar file handling functions like [[fopen()]], [[fread()]], [[fwrite()]], etc., to interact with ZIP files. Developers can directly access and manipulate the contents of a ZIP archive without needing to extract the files to a temporary location first. It's possible to read from and write to individual files within a ZIP archive, just like working with regular files.

Some examples of its usage include opening a file in a ZIP archive:

```php
$zip = 'zip://archive.zip#file.txt';
$file = fopen($zip, 'r');
$content = fread($file, 1000);
fclose($file);
```

> [!info]
> This opens a file named file.txt inside archive.zip, reads its content and closes the file.

Or creating a new file in a ZIP archive:

```php
$zip = 'zip://archive.zip#newfile.txt';
$file = fopen($zip, 'w');
fwrite($file, 'Hello, World!');
fclose($file);
```

!!! info
This creates a file "newfile.txt" inside "archive.zip" and writes Hello World! into it.

The PHP ZIP extension must be installed and enabled to use the ZIP PHP wrapper. While local ZIP archives can be modified, remote ZIP archives (accessed via [[HTTP Protocol]] or [[File Transfer Protocol|FTP]]) are read-only. For very large ZIP files, using the ZIP PHP wrapper might not be the most efficient approach due to memory usage and performance considerations.
