The [MySQL](../databases/mysql.md) Improved (MySQLi) extension is a relational database driver used in the [PHP](../programming/php.md) programming language to provide an interface with MySQL databases. It is specifically designed to work with MySQL versions 4.1 and above. 

The MySQLi extension offers various benefits and improvements over the older PHP MySQL extension, making it a better choice for new applications and development.

In addition to the standard procedural interface, MySQLi provides an object-oriented interface. This allows for more sophisticated, robust, and object-oriented database interactions. MySQLi supports prepared statements, which provide a more secure way to execute SQL queries. [Prepared statements](../databases/prepared.md) prevent [SQL injection](../security/sqli.md) attacks by separating SQL logic from the data being inputted.

MySQLi allows the execution of multiple SQL statements in a single function call, which can enhance performance by reducing the amount of round-trip communication between the PHP application and the MySQL server.

To use MySQLi, you must have PHP and MySQL installed on your server. The MySQLi extension is enabled by default on most PHP installations since PHP 5.0. A simple example is:

```php
$mysqli = new mysqli("localhost", "username", "password", "database");

if ($mysqli->connect_error) {
    die("Connection failed: " . $mysqli->connect_error);
}

$result = $mysqli->query("SELECT * FROM table");
while($row = $result->fetch_assoc()) {
    echo $row["column1"]. " - " . $row["column2"]. "<br>";
}

$mysqli->close();
```

