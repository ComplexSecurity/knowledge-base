The `require_once()` function in [[PHP]] is a control structure used to include the contents of another file into the script that is currently executing. It is very similar to the [[require()]] function, but with a crucial addition: it checks if the specified file has already been included, and if so, it will not include or require it again. 

This functionality is particularly useful for including files that contain code which should only be executed once, such as function definitions, class declarations, or variable initializations.

It ensures that the file is included only once. If the same file is attempted to be included again using `require_once()`, it will be ignored, preventing issues like function redefinitions or class redeclarations. Like `require()`, if the file cannot be found or is unavailable, `require_once()` generates a fatal error and halts the script execution. This is different from [[require_once()]], which emits a warning but allows the script to continue.

It is commonly used for including files where you need to ensure that the file is not included more than once. This is particularly important for files defining classes, functions, or setting up critical configuration settings.

The syntax is:

```php
require_once 'path/to/file.php';
```

A more realistic example is:

```php
<?php
// Require a file containing a class definition
require_once 'MyClass.php';

// Use the class
$myObject = new MyClass();

// Further code...
?>
```

>[!info] 
>In this example, `MyClass.php` is included only once, regardless of how many times `require_once 'MyClass.php';` is called. This prevents errors that would occur if the class `MyClass` were defined multiple times.

`require_once()` in PHP can be vulnerable to security risks, particularly if it's used with improperly validated or sanitized user input. The primary vulnerability associated with `require_once()` is [[Local File Inclusion]] (LFI), similar to the vulnerabilities in [[include()]], [[include_once()]], and [[require()]].

An example of vulnerable code is:

```php
<?php
// A vulnerable script where the file name is taken from user input
$page = $_GET['page'];
require_once($page . '.php');
?>
```

!!! caution
    In this example, an attacker could manipulate the query string in the URL to include arbitrary files from the server, such as `http://example.com/script.php?page=../../etc/passwd`. This could lead to sensitive data exposure.
  
A more secure implementation could be:

```php
<?php
// Define a whitelist of allowed files
$allowedFiles = [
    'home' => 'home.php',
    'contact' => 'contact.php',
    'about' => 'about.php'
];

// Get the user input, defaulting to a specific page if not provided
$pageKey = $_GET['page'] ?? 'home';

// Validate the user input against the whitelist
if (array_key_exists($pageKey, $allowedFiles)) {
    // Use the file from the whitelist
    require_once $allowedFiles[$pageKey];
} else {
    // Handle the error, such as showing an error message or redirecting
    echo 'Page not found.';
    // Alternatively, redirect to a default page or show a 404 page
}
?>
```

1. **Whitelisting**: The `$allowedFiles` array acts as a whitelist, ensuring that only predefined file paths are used. This prevents the possibility of including arbitrary files based on user input.
2. **Input Validation**: The script checks if the user-provided input (`$pageKey`) exists in the whitelist. If it doesn't, the script does not proceed with the `require_once()`.
3. **Default Values**: Using `$_GET['page'] ?? 'home'` ensures that there is always a valid value for `$pageKey`, preventing undefined index notices and ensuring a valid page is loaded by default.
4. **Error Handling**: If the input does not match any key in the whitelist, the script handles this gracefully, either by showing an error message or redirecting to a default or error page. This avoids exposing any sensitive server information.

