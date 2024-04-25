document.writeln() is a [JavaScript](../programming/js.md) method used to write a string of text to the document stream, followed by a newline character. It's part of the [Document Object Model (DOM)](../web/dom.md) and is closely related to the [document.write()](../programming/dwrite.md) method.

The primary difference is that writeln adds a newline character at the end of the string, which results in a line break in the rendered [HTML](../web/html.md).

The syntax of document.writeln() is similiar to document.write() - it takes one or more strings as arguments and writes them to the HTML document, adding a newline character at the end:

```javascript
document.writeln(string1, string2, ..., stringN);
```

A usage example would be:

```javascript
document.writeln("Hello, world!");
document.writeln("This is on a new line.");
```

This script will write "Hello, world!" to the document, then start a new line and write "This is on a new line.".

Just like document.write(), document.writeln() can pose security risks if used with untrusted data. It can be a vector for [Cross-Site Scripting (XSS)](../web/xss.md) attacks if the written data is not properly sanitized.
