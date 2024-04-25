document.write() is a [[JavaScript]] method used to write content directly to the [[HTML]] document. When called, it writes a string of text to the position in the document where the document.write() call is made. This method is often used to dynamically generate HTML content on a webpage.

document.write() is a method in JavaScript used to write a string of text directly to the HTML document where the script is being processed. It's part of the [[Document Object Model]] (DOM) and provides a way to dynamically generate and add content to a webpage.

The method is typically called with a string argument, which is inserted into the HTML document at the point where the document.write() call appears:

```javascript
document.write("<h1>Hello, World!</h1>");
```

This would write a heading element (\<h1>) with the text "**Hello, World!**" into the HTML document.

The primary security concern with document.write() is its potential use in [[Cross-Site Scripting]] (XSS) attacks. If document.write() is used to write unfiltered, user-supplied data to the document, it can lead to the execution of malicious scripts.

For instance, if a web application uses document.write() to display data from a URL parameter or user input without proper sanitization, an attacker could inject a script into this data.
