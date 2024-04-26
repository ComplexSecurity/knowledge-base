The `shell_exec` function in [PHP](../programming/php.md) is used to execute shell commands from a PHP script and return the complete output as a string. It's similar to the [exec](../programming/exec.md) function but with a key difference in how the output is handled. While `shell_exec` provides useful functionality for running external programs, it can pose serious security risks if not used correctly.

The primary security risk with `shell_exec` is the potential for [command injection](../security/commin.md) attacks. If user-provided data is not properly sanitized, an attacker can inject and execute malicious commands on the server.

`shell_exec` can execute any command that the server’s shell can execute, which can lead to unauthorized system access, data leakage, or server compromise.