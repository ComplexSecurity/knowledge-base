The [jQuery](../programming/jquery.md) add() function is used to add elements to a set of matched elements in a jQuery object. This method is useful for combining elements from different selectors or different parts of the document into a single jQuery collection, which can then be manipulated or iterated over in a unified way.

The basic syntax of the add() function is:

```javascript
$(selector).add(elements);
```

Where:

- selector - the initial jQuery selector
- elements - the elements to be added to the jQuery object. It can be a string representing a selector, a [Document Object Model](../web/dom.md) element, an [HTML](../web/html.md) string or another jQuery object.

The add() function is often used to combine elements from multiple selectors such as:

```javascript
$("div").add("p");
```

This selects all <div\> elements and then adds all <p\> elements to the same jQuery object. If you need to apply the same style or event handlers to a group of elements that don't share the same parent or class, you can use add() to group them together:

```javascript
$("#myDiv").add(".myClass").css("background-color", "yellow");
```

This will change the background color of both the element with id myDiv and all elements with the class myClass.

If add() is used to handle user-supplied input or content from untrusted sources without proper validation and sanitization, there could be a risk of [Cross-Site Scripting](../web/xss.md) attacks. For example, if HTML content created based on user input is added to the DOM using add(), it could include malicious scripts.
