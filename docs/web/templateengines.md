  
Template engines, in the context of web applications, are tools or libraries that facilitate the dynamic generation of [[HTML]] or other markup languages based on templates and data. They allow developers to separate the presentation layer (HTML or other markup) from the underlying logic and data, promoting a cleaner and more maintainable code structure. 

Template engines are commonly used in server-side web development to generate dynamic content that is sent to the client's browser.

Templates are predefined structures that contain placeholders or variables representing dynamic content. These placeholders are replaced with actual data during the rendering process. Template engines enable the dynamic generation of HTML or other markup by combining templates with data.

Template engines bind data to placeholders in templates, ensuring that the final output reflects the current state of the application or the requested data. Template engines promote the separation of concerns by isolating the presentation logic (templating) from business logic.

!!! info
    This separation makes code more modular, maintainable, and easier to understand.

Templates can be reused across multiple pages or components, leading to consistent design and layout. Template engines often support control structures such as conditionals (if statements) and loops, allowing for dynamic content generation based on logic.

Some template engines support partial templates or includes, allowing developers to break down complex layouts into smaller, reusable components. Template inheritance is a feature that enables the creation of a base template with common elements (e.g., header, footer) and the extension of this template in specific pages or views.

Popular Template Engines:

- [[Mustache]]: A logic-less template syntax that can be used in various programming languages.
- [[Handlebars]]: An extension of Mustache with additional features for logic and helpers.
- [[Jinja2]]: A template engine for Python commonly used in web frameworks like [[Flask]].
- [[EJS (Embedded JavaScript)]]: A simple templating language that embeds [[JavaScript]] code within templates.
- [[Thymeleaf]]: A [[Java]]-based template engine often used with [[Spring Framework]].

Template engines should handle user input carefully to prevent vulnerabilities such as [[Cross-Site Scripting]] (XSS). Proper escaping and sanitization are essential.