`bcrypt` is a cryptographic hashing algorithm used for securing passwords. It was designed to build a cryptographically secure hash that is resilient against brute-force search attacks, even with increasing computation power. 

The `bcrypt` algorithm is particularly notable for incorporating a [salt](../security/salt.md) (a random value) automatically and allowing the specification of a computational cost (work factor), which can be adjusted as hardware capabilities improve.

It automatically generates and applies a salt to each password. This prevents the use of [rainbow tables](../security/raintab.md) (precomputed tables used to crack [password hashes](../security/hashes.md)). It also allows the specification of the computational complexity (work factor), making the hash calculation slower. As hardware gets faster, the work factor can be increased to make [brute-force attacks](../security/brute.md) more difficult and time-consuming.

As computing power increases, the algorithm can be adjusted to be more computationally intensive, providing long-term security.

In [PHP](../programming/php.md), `bcrypt` is commonly used for password hashing and is accessible through the [password_hash()](../programming/passhash.md) and [password_verify()](../programming/passver.md) functions, which were introduced in PHP 5.5.0. These functions simplify secure password hashing and verification.

For example, hashing a password:

```php
$password = "user_password";
$hash = password_hash($password, PASSWORD_BCRYPT);
```

This creates a hashed version of the password using bcrypt.

You can also verify a password:

```php
$isPasswordCorrect = password_verify($password, $hash);
```

This checks a password against its hashed version and returns True if they match.

`bcrypt` is a robust algorithm that provides strong protection against [password cracking](../security/crack.md). PHP's built-in functions abstract the complexities of salt generation and hash comparison, reducing the risk of implementation errors. The ability to adjust the work factor means `bcrypt` can remain secure against increasing computational power.


 
