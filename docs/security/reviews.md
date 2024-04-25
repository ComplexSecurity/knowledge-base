Code reviews are a systematic examination of computer source code, intended to find and fix mistakes, improve the overall quality of the software, and ensure that it adheres to the established coding standards.

They are an integral part of the software development process and are typically conducted before merging code changes into the main project codebase.

In the context of web penetration testing (pentesting), code reviews are a detailed examination of a web application's source code to identify security vulnerabilities. Unlike automated scanning tools, code reviews involve a manual, line-by-line analysis of the code by security experts or developers.

This process is critical for uncovering issues that automated tools might miss, especially those related to logic flaws or complex security vulnerabilities.

Reviewers look for common security issues such as [[SQL injection]], [[Cross-Site Scripting]] (XSS), [[Cross-Site Request Forgery]] (CSRF), and other vulnerabilities that could be exploited by attackers.

It is also good to understand the business logic implemented in the code to ensure it does not introduce security vulnerabilities. Logical errors are often not detected by automated tools but can lead to significant security risks.

Checking how the application handles user authentication and authorization is also important, including session management, password handling, and access controls.
