The [[jQuery]] parseHTML() function is used to parse a string of [[HTML]] into an array of [[Document Object Model|DOM]] nodes. This function is particularly useful when you need to manipulate or examine HTML content provided as a string before inserting it into the document.

parseHTML() takes a string of HTML and parses it into a collection of DOM nodes. This allows you to manipulate the nodes using jQuery methods before they are inserted into the DOM.

The syntax is:

```javascript
$.parseHTML(htmlString, context, keepScripts)
```

- htmlString - HTML string to be parsed
- context - document in which the nodes will be created. Defaults to current document
- keepScripts - a boolean indicating whether to include script elements in the parsed HTML string. By default set to false to prevent script execution.

An example usage:

```javascript
var htmlString = "<div><p>Hello World</p></div>";
var htmlNodes = $.parseHTML(htmlString);
$("#someContainer").append(htmlNodes);
```

This example parses the **htmlString** into DOM nodes and appends them to an element with the ID **someContainer**.

Since parseHTML() does not execute scripts by default, it provides a safer way to handle HTML strings that might contain \<script> tags, helping to mitigate [[Cross-Site Scripting]] (XSS) vulnerabilities.

Even though parseHTML() does not execute scripts by default, you should still sanitize the input HTML string to prevent XSS attacks, especially if the HTML is from an untrusted source.