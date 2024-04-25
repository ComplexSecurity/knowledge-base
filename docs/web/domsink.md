In the context of the [[Document Object Model]] (DOM), "sinks" are points in the application where data is output or where the data can lead to code execution. These are functions or properties that can dynamically change the content of the web page or execute code based on the provided input.

Some examples include:

- innerHTML - sets or returns the [[HTML]] content of a element. Writing to it can potentially execute malicious scripts if the input is not properly sanitized.
- document.write - writes HTML expressions or [[JavaScript]] code to a document. Can be harmful if the data written is untrusted.
- eval - executes a string as JavaScript code, which is a significant security risk if the string contains untrusted data.
- setTimeout and setInterval - can evaluate strings as code, posing a risk if the string is constructed from unsafe sources.

The main risk with DOM sinks is the possibility of executing untrusted data as code. This is the primary mechanism through which [[Cross-Site Scripting|XSS]] attacks are conducted. When a sink like innerHTML is used with data from an unsafe source, it can lead to script injection and the execution of malicious scripts.
