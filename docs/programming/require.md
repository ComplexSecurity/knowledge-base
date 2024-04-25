The `require()` function in [[PHP]] is used to include and execute the contents of a specified file during the execution of a script. It's very similar to the [[include()]] function, but with a key difference in how it handles errors.

If `require()` fails to find or open the specified file, it generates a fatal error and halts the execution of the script. This is in contrast to `include()`, which only emits a warning (**E_WARNING**) and the script will continue to execute. `require()` is commonly used when the file is essential for the application to run. For example, files containing necessary functions, classes, or configurations are typically included using `require()`.

If the same file is `require()`d multiple times within a script, the file's contents will be executed each time it is called. To prevent this, `require_once()` can be used, which ensures that the file is included only once.

The syntax is:

```php
require 'path/to/file.php';
```

A more realistic example may be:

```php
<?php
// Include a critical configuration file
require 'config.php';

// Rest of the script that depends on the configuration settings
?>
```

The `require()` function in PHP can be vulnerable to security risks, similar to [[include()]] and [[include_once()]]. The primary vulnerability associated with `require()` is [[Local File Inclusion]] (LFI), which can occur if the function is used with improperly validated or sanitized user input.

An example of a vulnerable use:

```php
<?php
// A vulnerable script where the file name is taken from user input
$page = $_GET['page'];
require($page . '.php');
?>
```

!!! danger
    In this example, if a user can control the value of `$_GET['page']`, they might be able to include files like `config.php` by manipulating the URL, such as `http://example.com/?page=../config`.

A more secure implementation may look like:

```php
<?php
// Define a whitelist of allowed files
$allowedPages = [
    'home' => 'home.php',
    'contact' => 'contact.php',
    'about' => 'about.php'
];

// Get the user input
$page = $_GET['page'] ?? 'default'; // Default page if none is specified

// Validate the user input against the whitelist
if (array_key_exists($page, $allowedPages)) {
    // Use the file from the whitelist, ensuring the input cannot affect the file path
    require $allowedPages[$page];
} else {
    // Handle the error or redirect to a default page
    echo 'Page not found.';
    // Or you can redirect to a default page like this:
    // header('Location: default.php');
    // exit();
}
?>
```

1. **Whitelisting**: Only files listed in `$allowedPages` are allowed to be included. This prevents attackers from including arbitrary files.
2. **Validation**: The user input (`$page`) is checked against the whitelist. This ensures that only predefined paths can be used in `require()`.
3. **Default Values**: The use of `$_GET['page'] ?? 'default'` ensures that there is always a valid value for `$page`. If the user does not provide input, it defaults to 'default'.
4. **Error Handling**: If the user input does not match any key in the whitelist, the script handles this gracefully by displaying an error message or redirecting to a default page.

