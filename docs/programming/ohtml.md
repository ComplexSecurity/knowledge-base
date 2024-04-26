DOM.outerHTML is a property in the [Document Object Model (DOM)](../web/dom.md) of [HTML](../web/html.md) and [XML](../programming/xml.md) documents that represents the serialized HTML or XML source of the element, including the element itself.

This property is used in web development to get or set the markup of the element and all its children.

When used to get the content, outerHTML returns a string containing the markup of the element, including its opening and closing tags, attributes, and all its child elements.

For example, if you have an element defined as:

```html
<div id="example">
  \
  <p>Hello\</p>
</div>
```

Using outerHTML on this element would return the entire string:

```html
<div id="example">
  \
  <p>Hello\</p>
</div>
```

When outerHTML is used to set the content of an element, it replaces the entire element (including itself) with the new content provided:

```javascript
document.getElementById("example").outerHTML = "<span>New content</span>";
```

This would replace the entire <div id="example"\> element with <span\>New content</span\>.

In comparison with [DOM.innerHTML](../programming/innerh.md) which gets or sets the HTML or XML markup contained within the element excluding the element itself, DOM.outerHTML gets or sets the HTML or XML markup of the element including the element itself.

When setting outerHTML with user-supplied data, there's a risk of [Cross-Site Scripting (XSS)](../web/xss.md) if the data isn't properly sanitized. It's crucial to ensure that any dynamic content inserted through outerHTML is safe and free from malicious scripts.
