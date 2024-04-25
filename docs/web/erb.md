ERB, which stands for "Embedded Ruby", is a templating system that is part of the standard library for the [[Ruby]] programming language. It allows Ruby code to be embedded within a text document, typically [[HTML]]. This can be particularly useful in web development for dynamically generating webpage content.

ERB lets you embed Ruby code into a text file, usually an HTML file, to create dynamic content. The Ruby code is evaluated, and the output is inserted into the document in place of the code itself.

ERB uses tags to denote the Ruby code that should be evaluated. The most common tags are `<% %>` and `<%= %>`.

- `<% %>`: This tag runs Ruby code but doesn't output anything to the final text. It's used for logic like loops and conditionals.
- `<%= %>`: This tag runs Ruby code and outputs the result to the document. It's often used for displaying variable values or results of Ruby expressions.

In Ruby web frameworks like [[Ruby on Rails]], ERB is commonly used for creating views. It allows developers to write HTML templates with embedded Ruby code to generate dynamic web pages based on user requests and data from a database.

A simple ERB template might look like this:

```ruby
<html>
<body>
  <h1>Welcome, <%= @user.name %></h1>
</body>
</html>
```

In this example, `@user.name` is a Ruby expression whose value is displayed within the `<h1>` tag. ERB enables a clear separation of HTML structure from the Ruby code used for business logic, adhering to the principle of separation of concerns in software development.

ERB can be used in various contexts, not just for web pages. It's suitable for any scenario where dynamic content generation is needed. While ERB is part of the standard Ruby library, it is particularly prominent in Ruby on Rails applications, where it's the default templating engine for generating HTML.
