Template directives are commands or instructions embedded within a template that guide the [[Template Engines]] on how to process and render the content. These directives provide additional logic and control over the template's behavior, allowing developers to define conditions, loops, and other dynamic behaviors within the static structure of the template. 

The specific syntax and capabilities of directives depend on the template engine being used.

Some common types of template directives:

Conditionals ([[Handlebars]]):

```handlebars
{{#if condition}}
  <!-- Content to display if the condition is true -->
{{else}}
  <!-- Content to display if the condition is false -->
{{/if}}
```

Conditionals ([[Jinja2]]):

```python
{% if condition %}
  {# Content to display if the condition is true #}
{% else %}
  {# Content to display if the condition is false #}
{% endif %}
```

Loops (Handlebars):

```handlebars
{{#each items}}
  <!-- Content to repeat for each item in the 'items' array -->
{{/each}}
```

Loops (Jinja2):

```python
{% for item in items %}
  {# Content to repeat for each item in the 'items' list #}
{% endfor %}
```

Variable Output (Handlebars):

```handlebars
{{variable}}
```

Variable Output (Jinja2):

```python
{{ variable }}
```

Partial Templates (Handlebars):

```handlebars
{{> partial}}
```

Partial Templates (Jinja2):

```python
{% include 'partial.html' %}
```

Template Inheritance (Jinja2):

```python
{% extends 'base.html' %}
{% block content %}
  {# Content specific to this template #}
{% endblock %}
```

Comments (Handlebars):

```handlebars
{{!-- This is a comment in Handlebars --}}
```

Comments (Jinja2):

```python
{# This is a comment in Jinja2 #}
```

Escaping and Raw Output (Handlebars):

```handlebars
{{{rawHtml}}} <!-- Outputs HTML without escaping -->
```

Escaping and Raw Output (Jinja2):

```python
{{ rawHtml | safe }} {# Outputs HTML without escaping #}
```