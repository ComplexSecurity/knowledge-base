In [PHP](../programming/php.md), the `php://input` stream allows you to read raw POST data. It is less memory intensive than `$HTTP_RAW_POST_DATA` and does not need any special `php.ini` directives. `php://input` is not available with `enctype="multipart/form-data"`.

It provides access to raw POST data, which is useful when you need to process the body of a POST request directly, such as with [JSON](../misc/json.md) or [XML](../programming/xml.md) payloads. It's a read-only stream that can only be read once, as it does not support seek operations. However, as of PHP 5.6, it can be reopened and read multiple times.

Unlike `$_POST`, which is affected by certain `php.ini` settings (like `post_max_size`), `php://input` allows access to the raw POST data without processing.

The `php://input` stream is often used for reading JSON or XML POST data, which is common in [REST APIs](../web/restapis.md) and web services:

```php
<?php
// Example - Reading JSON POST data

// Get the raw POST data
$rawData = file_get_contents("php://input");

// Decode the JSON data
$jsonData = json_decode($rawData);

// Use the JSON data
if ($jsonData) {
    // Process the JSON data
    echo "Received: " . print_r($jsonData, true);
} else {
    echo "No valid JSON data received";
}
?>
```

!!! info
    In this example, `file_get_contents("php://input")` is used to read the raw POST data. This is particularly useful for content types that are not automatically parsed by PHP, like JSON or XML.

`php://input` is an essential feature for modern PHP applications, particularly those that interact with [APIs](../terms/apis.md) or rely on [AJAX](../web/ajax.md) requests. It provides a more straightforward and efficient way of accessing raw POST data compared to older methods.

The `php://input` stream itself in PHP is not inherently vulnerable. However, like any data input in web applications, its use can introduce security vulnerabilities if the data is not properly handled. The security risk primarily arises from how the input data is processed and used within the application, rather than from the `php://input` stream itself.

If the data read from `php://input` is not properly sanitized, it can lead to various security issues like [SQL Injection](../security/sqli.md), [Cross-Site Scripting (XSS)](../web/xss.md), or [XML External Entity (XXE)](../web/xxe.md) Injection, depending on how the data is used. Reading large amounts of data from `php://input` without proper size checks can lead to [buffer overflow](../security/buffer.md) or resource exhaustion issues.

Consider a PHP script that reads JSON data from `php://input` and uses it in a database query without proper validation or sanitization:

```php
<?php
// Example of a potentially vulnerable use of php://input

// Get the raw POST data
$rawData = file_get_contents("php://input");
$data = json_decode($rawData, true);

// Unsafe database query
$query = "SELECT * FROM users WHERE id = " . $data['id'];
$result = mysqli_query($connection, $query);
?>
```

In this example, if the `id` parameter from the input data is not properly sanitized, it could be exploited for SQL Injection attacks. An attacker could potentially manipulate the `id` parameter in the raw POST data to alter the SQL query, leading to unauthorized database access or manipulation.

