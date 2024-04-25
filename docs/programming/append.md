The [jQuery](../programming/jquery.md) append() function is used to insert content at the end of the selected elements within the DOM ([Document Object Model](../web/dom.md)). It is a widely used method in jQuery for dynamically adding new content or elements to a webpage.

The append() function can take a string of [HTML](../web/html.md), a DOM element, an array of elements, a jQuery object, or a function as an argument. The content specified in the argument is then inserted at the end of each element in the set of matched elements:

```javascript
$(selector).append(content);
```

Where:

- selector - the jQuery selector identifying the elements to which the new content will be appended.
- content - the content to be appended, can be HTML strings, DOM elements, other jQuery objects or a function that returns content to append.

An example could be:

```javascript
$("#myDiv").append("<p>New paragraph</p>");
```

This will add a new paragraph (**<p\>New paragraph</p\>**) to the end of the element with the ID myDiv.

The append() function can also take multiple arguments or a combination of different types of arguments to append multiple elements simultaneously. When appending content based on user input or external sources, be cautious of [Cross-Site Scripting](../web/xss.md) (XSS) vulnerabilities. Always sanitize external input to prevent the injection of malicious code.
