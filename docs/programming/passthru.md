The `passthru` function in [[PHP]] is used to execute an external program and display raw output. It's one of the several PHP functions that allow for running system commands, similar to [[exec]] and [[shell_exec]], but with some differences in behavior and output handling.

`passthru` is specifically used when you want to execute a system command that outputs binary data or needs to pass the output directly back to the browser. Unlike `exec`, which collects the command output and allows you to process it within PHP, `passthru` sends the output directly to the browser. This makes it suitable for executing commands that produce binary output, like displaying an image or a PDF file.

Like other command execution functions, `passthru` is vulnerable to [[command injection]] attacks. If user-supplied input is incorporated into the command without proper [[Input Sanitization|sanitization]], it can lead to severe security vulnerabilities.

Since `passthru` sends output directly to the browser, there is a risk of exposing sensitive information if not carefully handled. A typical use of `passthru` might be to execute system commands for tasks that require real-time output to be sent to the client, such as streaming video or audio data.

PHP offers other functions for executing external programs, such as exec, shell_exec, and [[system]], each with specific use cases and output handling characteristics.