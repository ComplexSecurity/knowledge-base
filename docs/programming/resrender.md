The `res.render()` function is used in [[Express|Express.js]], a web framework for [[NodeJs|Node.js]]. It is a method of the response object (`res`) that compiles your template (written in a view engine like [[EJS (Embedded JavaScript)|EJS]], [[Pug (Jade)|Pug]], [[Handlebars]], etc.), inserts variables into it, and sends the resulting [[HTML]] string as the response.

`res.render()` is used to render a view (template) and send its HTML output to the client. It works with different view engines supported by Express.js. The choice of view engine (like EJS, Pug, Handlebars) determines the syntax and capabilities of your templates.

You can pass a JavaScript object as the second argument to `res.render()`, which contains data to be inserted into the template. This makes it dynamic and responsive to each request. Many view engines support layouts and partials, which allow for reusable template pieces and consistent layout structures across different views.

The syntax is:

```js
res.render(view [, locals] [, callback])
```

- `view`: A string that is the file path of the view file to render. This path is relative to the views directory you set in your Express.js configuration.
- `locals` (Optional): An object containing properties that the view will use to render dynamic content.
- `callback` (Optional): A callback function that lets you handle the rendered HTML string manually, rather than sending it as the HTTP response.

As an example, assume you are using EJS as your view engine:

```js
app.get('/', function (req, res) {
    res.render('index', { title: 'Home', message: 'Welcome to the Home Page' });
});
```

In this example, `res.render()` is used to render the `index` view. The second argument is an object with properties `title` and `message`, which are variables used in the `index.ejs` template to dynamically generate the HTML content.

The `res.render()` function in Express.js itself is not inherently vulnerable. However, vulnerabilities can arise based on how it's used, particularly when dealing with user-provided data. The primary security concern in the context of `res.render()` and [[Template Engines|templating engines]] is [[Cross-Site Scripting]] (XSS).

Suppose you have a route in your Express.js application that takes a query parameter and renders it directly onto the page:

```js
app.get('/somepage', function (req, res) {
    // User input is taken directly from the query parameter
    const userInput = req.query.userInput;

    // This could be dangerous if userInput contains malicious script
    res.render('somepage', { userInput });
});
```
!!! caution
    In this scenario, if `userInput` is not properly escaped and contains JavaScript code, it will be rendered as-is into the HTML. An attacker could exploit this by crafting a URL with a script in the `userInput` parameter. For example:

```bash
http://example.com/somepage?userInput=<script>maliciousCode()</script>
```

