PHP Filters are a feature in [PHP](../programming/php.md) used to validate and sanitize external input. This feature is essential for securing PHP applications by ensuring that input data is safe before using it. PHP Filters are especially useful in preventing security vulnerabilities like [SQL injection](../security/sqli.md), [cross-site scripting (XSS)](../web/xss.md), and other common input-related attacks.

The types of filters include:

1. **Validation Filters**: These filters are used to validate input data. They check if the data meets certain criteria (like being a valid email address, an integer, a boolean, etc.) but don't modify the data itself. Examples include `FILTER_VALIDATE_EMAIL`, `FILTER_VALIDATE_INT`, `FILTER_VALIDATE_URL`, etc.
2. **Sanitization Filters**: These filters are used to sanitize input data, which means they clean or modify the data to ensure there's nothing harmful (like stripping out HTML tags or encoding special characters). Examples include `FILTER_SANITIZE_STRING`, `FILTER_SANITIZE_EMAIL`, `FILTER_SANITIZE_URL`, etc.
3. **Other Filters**: PHP also provides other filters for specialized purposes, like `FILTER_CALLBACK`, which allows you to apply a custom function to the data.

Some examples include validating an email address:

```php
$email = "test@example.com";
if (filter_var($email, FILTER_VALIDATE_EMAIL)) {
    echo "This is a valid email address.";
} else {
    echo "This is not a valid email address.";
}
```

Or sanitizing a string:

```php
$dirty_string = "<script>alert('xss');</script>Some text";
$clean_string = filter_var($dirty_string, FILTER_SANITIZE_STRING);
echo $clean_string;  // Output will be "alert('xss');Some text"
```

Or filtering an integer and validating range:

```php
$options = array(
    "options" => array(
        "min_range" => 1,
        "max_range" => 100
    )
);
$number = 50;
if (filter_var($number, FILTER_VALIDATE_INT, $options)) {
    echo "The number is within the specified range.";
} else {
    echo "The number is not within the specified range.";
}
```

