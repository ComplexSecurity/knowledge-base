The `include()` function in [PHP](../programming/php.md) is a widely-used construct that allows a PHP file to insert and execute the content of another file into the current file. This is particularly useful for reusing code, such as headers, footers, or user-defined functions, across multiple pages of a website.

The `include()` function can be a security risk if not properly handled, especially in scenarios where the file to be included is determined by user input. This risk arises from a vulnerability known as "[Local File Inclusion](../web/lfi.md)" (LFI) or, in some cases, "[Remote File Inclusion](../security/rfi.md)" (RFI):

1. **Local File Inclusion (LFI)**: This occurs when a script allows user-controlled input to dictate which files are included. An attacker could exploit this to include files that are already on the server, such as configuration files containing sensitive information.
2. **Remote File Inclusion (RFI)**: This is possible if the `include()` function is configured to allow the inclusion of remote files (files located on a different server). An attacker can use this to include malicious files from a remote server, leading to various attacks such as code execution, data theft, or server compromise.

A basic example may be:

```php
// This will include 'header.php' in the current file.
include('header.php');

// Rest of the page content goes here

// This will include 'footer.php' in the current file.
include('footer.php');
```

Whereas a vulnerable example may be:

```php
// A more secure approach using whitelisting
$allowed_pages = ['home', 'contact', 'about'];
$page = $_GET['page'];

if (in_array($page, $allowed_pages)) {
    include($page . '.php');
} else {
    echo 'Page not found.';
}
```

!!! danger
    In this example, if a user can control the value of `$_GET['page']`, they might be able to include files like `config.php` by accessing the URL `http://example.com/?page=../config`.

A more secure example may be:

```php
// A more secure approach using whitelisting
$allowed_pages = ['home', 'contact', 'about'];
$page = $_GET['page'];

if (in_array($page, $allowed_pages)) {
    include($page . '.php');
} else {
    echo 'Page not found.';
}
```

In this secure example, the `include()` only happens if the user input matches one of the predefined and allowed pages, significantly reducing the risk of LFI attacks.

