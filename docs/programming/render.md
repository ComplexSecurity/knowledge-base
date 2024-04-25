In the [[Express]] framework for [[NodeJs|Node.js]], the `render()` function is used in the context of server-side rendering. It is a method of the response object (`res`) provided by Express to render a view template. When you call `res.render()`, Express compiles the specified template using the configured template engine, injects local variables into the template, and sends the generated [[HTML]] string as the response to the client.

Express supports various [[template engines]] like [[EJS (Embedded JavaScript)|EJS]], [[Pug (Jade)]], [[Handlebars]], etc. The choice of template engine determines the syntax and features available in your templates. The `render()` function takes a template file and a data object. It combines them to produce a complete HTML page which includes dynamic data. The resulting HTML from the rendering process is automatically sent back to the client as the response.

The syntax is:

```js
res.render(view [, locals] [, callback])
```

- `view`: The name of the view file to be rendered. This does not typically include the file extension, as that is inferred from the view engine setup.
- `locals` (Optional): An object containing response local variables - data that you want to pass to the view for rendering.
- `callback` (Optional): A callback function that gets called when the render process is complete. If provided, the method will not send the rendered HTML automatically, allowing for further manipulation.

An example:

```js
const express = require('express');
const app = express();

app.set('view engine', 'ejs'); // Set EJS as the template engine

app.get('/', (req, res) => {
    // Render the 'index' view, passing 'title' and 'message' as data
    res.render('index', {
        title: 'Welcome',
        message: 'Hello to EJS!'
    });
});

app.listen(3000, () => console.log('Server running on port 3000'));
```

!!! info
    In this example, when a user visits the root URL (`'/'`), the server will render the `index.ejs` file, injecting the `title` and `message` data into it, and send the resulting HTML as the response.

The `render()` function in Express itself is not inherently vulnerable. However, vulnerabilities can arise based on how it's used, especially when rendering data that includes user input. The primary security concern in such scenarios is [[Cross-Site Scripting]] (XSS).

Consider an Express app using a templating engine like EJS, where user input is directly included in the rendered output without proper escaping:

```js
app.get('/profile', (req, res) => {
    // User input taken directly from the query string
    const username = req.query.username;

    // Rendering the username in the response without escaping
    // This could be dangerous if username contains malicious script
    res.render('profile', { username });
});
```

!!! danger
    In this scenario, if an attacker provides a username in the query string that contains JavaScript code, this code will be rendered as-is into the HTML. If another user visits a URL like `http://example.com/profile?username=<script>maliciousCode()</script>`, the script would execute in their browser.

