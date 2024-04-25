The `include_once()` function in [[PHP]] is similar to the [[include_once()]] function, but with a key difference: it checks if the specified file has already been included, and if so, it does not include it again. 

This behavior is particularly useful in situations where the same file might be included multiple times due to complex scripting or nested includes. By using `include_once()`, you can prevent issues like function redefinitions, variable redeclarations, and performance overhead from redundant inclusions.

The syntax is:

```php
include_once 'path/to/file.php';
```

If a file containing functions is included multiple times, PHP will generate an error because it does not allow function redefinitions. Using `include_once()` ensures that the file is included only once, avoiding such errors. It's common to use `include_once()` for including configuration files. Since these files usually set up environment variables, database connections, or other critical settings, they should not be included more than once.

When dealing with object-oriented programming in PHP, `include_once()` is often used to include class definitions. This ensures that a class is not declared more than once, which would result in a fatal error.

An example includes:

```php
// Include a configuration file - it will only be included once, 
// even if this line appears multiple times in the script or in different scripts
// that are included in the execution flow.
include_once 'config.php';

// Further code that might also include 'config.php' directly or indirectly
```

While `include_once()` and [[require_once()]] serve similar purposes, the key difference lies in their behavior when the specified file cannot be found or loaded:

- `include_once()` will emit a warning (**E_WARNING**) and the script will continue to execute.
- `require_once()` will emit a fatal error (**E_COMPILE_ERROR**) and halt script execution.

The primary risks are similar to those with `include()`, notably [[Local File Inclusion]] (LFI) and [[Remote File Inclusion]] (RFI) vulnerabilities. However, the `include_once()` function's unique behavior does not inherently mitigate these risks.

A vulnerable example may be:

```php
<?php
// A vulnerable script where the file name is taken directly from user input
$page = $_GET['page'];

// Using include_once with user-controlled input
include_once($page . '.php');
?>
```

!!! danger
    In this script, the `$page` variable is directly taken from the user input (`$_GET['page']`). An attacker could manipulate the URL to include files that are not intended to be accessible. For example, if the script is located at `http://example.com/script.php`, an attacker could access the following URL to potentially include sensitive files:

```bash
http://example.com/script.php?page=../../etc/passwd
```

This URL attempts to traverse the directory structure (using `../` for going up a directory) and include the Unix/Linux system file `/etc/passwd`, which contains user information and could be sensitive.

An example of safe implementation includes:

```php
$allowed_pages = ['home', 'contact', 'about'];
$page = $_GET['page'];

if (in_array($page, $allowed_pages)) {
    include_once($page . '.php');
} else {
    echo 'Page not found.';
}
```

!!! success
    In this example, even though `include_once()` is used, the script ensures that only files from a predefined list are included, thus significantly reducing the risk of LFI attacks.

