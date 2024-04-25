Pug (formerly known as Jade) is a high-performance, feature-rich templating engine for [[NodeJS|Node.js]] and browsers. It's designed to facilitate writing [[HTML]] in a more efficient and readable manner. Pug templates use a simpler, whitespace-sensitive syntax with fewer characters and less repetition compared to plain HTML.

Pug offers a clean and concise syntax, using indentation instead of closing tags, making the templates easier to read and write. It allows dynamic content rendering, meaning you can pass variables and objects from your Node.js application to the template, and Pug will render the HTML accordingly.

Pug supports various control structures like conditionals and loops, which can be embedded directly in the template. It supports template inheritance, which is a powerful feature for reusing template code. You can define a base template (layout) and extend it in other templates. 

These are akin to functions in programming languages and can be used to create reusable pieces of template code. Pug allows you to use filters to pre-process text blocks, such as markdown or stylus.

Pug syntax is different from traditional HTML. It’s whitespace-sensitive and uses indentation to indicate nesting of elements, which eliminates the need for closing tags.

Example of a basic Pug template:

```js
doctype html
html(lang="en")
  head
    title= pageTitle
  body
    h1 Pug - Node Template Engine
    #container.col
      if user
        p Welcome, #{user}!
      else
        p Welcome, guest!
```

This template would render into the following HTML:

```js
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>[Value of pageTitle]</title>
  </head>
  <body>
    <h1>Pug - Node Template Engine</h1>
    <div id="container" class="col">
      <!-- Content based on the 'user' variable -->
      [Dynamic content based on the presence of 'user']
    </div>
  </body>
</html>
```

To use Pug in a Node.js application (like an Express.js app), you typically set Pug as the view engine and then render templates in response to requests.

```js
const express = require('express');
const app = express();

app.set('view engine', 'pug');

app.get('/', (req, res) => {
  res.render('index', { pageTitle: 'Home', user: 'John Doe' });
});

app.listen(3000);
```

>[!info]
>In this example, `res.render('index', { pageTitle: 'Home', user: 'John Doe' })` will render the `index.pug` file, injecting the `pageTitle` and `user` values into it.

