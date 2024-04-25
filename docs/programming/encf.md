[[PHP]] does provide various functions and libraries for handling encryption and cryptographic operations. These are not implemented as "filters" in the same sense as PHP's data validation and sanitization filters, but they serve the purpose of encrypting and decrypting data.

1. **penSSL Functions**: PHP's [[OpenSSL]] extension offers a comprehensive set of functions for encryption and decryption, as well as for other cryptographic operations like generating certificates, signing data, etc. Functions like `openssl_encrypt()` and `openssl_decrypt()` are used for encrypting and decrypting data respectively.
2. **Sodium Library**: Introduced in PHP 7.2, the [[Sodium]] library is a modern and easy-to-use cryptographic library that provides a higher level of security. It offers various encryption functions, including public-key and symmetric-key encryption.
3. **Mcrypt Functions**: Although it was deprecated in PHP 7.1 and removed in PHP 7.2, the [[Mcrypt]] extension was previously widely used for encryption. It's not recommended for use in newer PHP versions, but it's worth mentioning for legacy applications.
4. **Hash Functions**: While not encryption per se, PHP provides functions like `hash()` and `password_hash()` for generating cryptographic hashes of data, which is essential for securely storing passwords and other sensitive information.
5. **Custom Encryption/Decryption Functions**: PHP allows you to create custom encryption and decryption mechanisms using the available cryptographic libraries and functions, tailored to the specific needs of your application.

Some examples include using OpenSSL for encryption:

```php
$data = "Secret Data";
$encryption_key = openssl_random_pseudo_bytes(32);
$iv = openssl_random_pseudo_bytes(openssl_cipher_iv_length('aes-256-cbc'));
$encrypted = openssl_encrypt($data, 'aes-256-cbc', $encryption_key, 0, $iv);
$decrypted = openssl_decrypt($encrypted, 'aes-256-cbc', $encryption_key, 0, $iv);
```

Or using Sodium for encryption:

```php
$key = sodium_crypto_secretbox_keygen();
$nonce = random_bytes(SODIUM_CRYPTO_SECRETBOX_NONCEBYTES);
$cipher = sodium_crypto_secretbox('Sensitive data', $nonce, $key);
$original = sodium_crypto_secretbox_open($cipher, $nonce, $key);
```
