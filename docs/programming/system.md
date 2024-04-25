The `system` function in [[PHP]] is used to execute an external program or command and display the output. It's part of PHP's functionality for interfacing with the underlying operating system. Like other similar functions ([[exec]], [[shell_exec]], [[passthru]]), `system` allows PHP scripts to run system-level commands, but with specific behavior and output handling.

The `system` function is designed to display the output of the command directly to the browser (or wherever the PHP script output goes). This makes it suitable for commands where you want to see the full output as it's generated.

The primary security risk with `system` is [[command injection]]. If user input is incorporated into the command without proper sanitization, it can lead to execution of arbitrary and potentially harmful commands. Because `system` outputs directly, there's a risk of disclosing sensitive information if the command's output is not properly handled or restricted.

`system` might be used for tasks that require the output of system commands, like getting the status of system resources, provided that the output is non-sensitive.