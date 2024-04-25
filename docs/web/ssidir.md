Server-Side Includes (SSI) directives are commands used in web development to include dynamic content or execute server-side scripts within [[HTML]] documents. These directives are processed by the web server before sending the content to the client's browser. SSI directives are typically used to modularize and enhance the functionality of web pages. 

1. **Include Directive (`<!--#include -->`):**
    - Syntax: `<!--#include virtual="file_path" -->`
    - This directive includes the content of another file into the current HTML document.
    - Example: `<!--#include virtual="/includes/header.html" -->`
2. **Echo Directive (`<!--#echo -->`):**
    - Syntax: `<!--#echo var="variable_name" -->`
    - This directive displays the value of a specified server variable or environment variable.
    - Example: `<!--#echo var="REMOTE_ADDR" -->`
3. **If Directive (`<!--#if -->`):**
    - Syntax: `<!--#if expr="conditional_expression" --> ... <!--#endif -->`
    - Allows conditional execution of content based on a specified condition.
    - Example:

```html
<!--#if expr="${QUERY_STRING='show'}" -->
  This content is displayed when the 'show' parameter is present in the query string.
<!--#endif -->
```

1. **Set Directive (`<!--#set -->`):**
    - Syntax: `<!--#set var="variable_name" value="new_value" -->`
    - Sets the value of a server variable or environment variable for later use.
    - Example: `<!--#set var="my_variable" value="Hello, World!" -->`
2. **Config Directive (`<!--#config -->`):**
    - Syntax: `<!--#config option="directive_name" value="directive_value" -->`
    - Configures various settings for SSI processing.
    - Example: `<!--#config timefmt="%A, %B %d, %Y" -->`
3. **Include Virtual Directive (`<!--#include virtual -->`):**
    - Similar to the `include` directive but uses a virtual path instead of a file system path.
    - Syntax: `<!--#include virtual="/virtual_path/file.html" -->`
4. **FSize Directive (`<!--#fsize -->`):**
    - Syntax: `<!--#fsize file="file_path" -->`
    - Displays the size of a specified file.
    - Example: `<!--#fsize file="/images/logo.png" -->`
5. **Flastmod Directive (`<!--#flastmod -->`):**
    - Syntax: `<!--#flastmod file="file_path" -->`
    - Displays the last modification date of a specified file.
    - Example: `<!--#flastmod file="/documents/report.doc" -->`

