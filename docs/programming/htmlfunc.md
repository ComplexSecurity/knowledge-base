The [jQuery](../programming/jquery.md) html() function is used to get or set the [HTML](../web/html.md) content of an element. It's a versatile and widely-used function in jQuery, a popular [JavaScript](../programming/js.md) library, for [DOM](../web/dom.md) manipulation.

When used without any arguments, html() gets the HTML content of the first element in the set of matched elements:

```javascript
var content = $(selector).html();
```

An example:

```javascript
var content = $('#myDiv').html();
```

This retrieves the inner HTML content of the element with the ID myDiv. When a string is passed as an argument to html(), it sets the HTML content of each element in the set of matched elements to the specified string:

```javascript
$(selector).html(htmlString);
```

An example:

```javascript
$('#myDiv').html('<p>New content</p>');
```

This example sets the inner HTML of the element with the ID myDiv to \<p>New content\</p>.

If you use html() with user-supplied data or content from an untrusted source, it poses a risk of [XSS](../web/xss.md) attacks. You should always sanitize input to ensure it's safe before using it with html().