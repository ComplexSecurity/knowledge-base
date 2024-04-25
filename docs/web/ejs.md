Embedded JavaScript (EJS) is a [[Template Engines|templating language]] that allows developers to embed [[JavaScript]] code directly within [[HTML]] markup. It enables the dynamic generation of HTML content by incorporating server-side logic directly into the templates. EJS is often used in web development frameworks that follow the [[NodeJS|Node.js]] ecosystem, but it can be used in various environments where JavaScript is supported.

EJS allows developers to embed JavaScript code within `<% %>` tags in HTML files. This embedded code can include variables, loops, conditionals, and other JavaScript expressions.

Example:

```html
<ul>
  <% for (let i = 0; i < items.length; i++) { %>
  <li><%= items[i] %></li>
  <% } %>
</ul>
```

To output dynamic content securely, EJS provides `<%= %>` tags. Content within these tags is HTML-escaped by default, preventing potential cross-site scripting (XSS) vulnerabilities.

Example:

```html
<p>Name: <%= user.name %></p>
```

EJS supports control flow structures such as if, else, for, and more. This allows developers to create dynamic templates with conditional logic and iterations.

Example:

```html
<% if (user.isAdmin) { %>
<p>Welcome, admin!</p>
<% } else { %>
<p>Welcome, user!</p>
<% } %>
```

EJS allows the inclusion of other templates or partials using <%- include('partial.ejs') %>. This promotes code reuse and modularization.

Example:

```html
<header><%- include('header.ejs') %></header>
```

Developers can define custom tags and functions to extend EJS's functionality. This provides flexibility in creating reusable components and helpers.

Example:

```html
<p><%= customFunction(data) %></p>
```

EJS is lightweight, easy to use, and integrates seamlessly with Node.js applications. It is commonly used for server-side rendering (SSR) in web frameworks like [[Express|Express.js]]. Additionally, EJS templates can be rendered on the server side or client side, depending on the use case.
