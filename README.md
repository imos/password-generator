Introduction
============

password-generator is a command-line tool to use a different password for every site.

* Web version - http://imoz.jp/password.html

Usage
=====

```sh
$ password-generator 
Master password: ← Type your master password here
Password hash is 6nAeqHv2. Right? [Y/n] ← Press Enter key if it is correct.
Domain: github.com ← Type a domain in lower case.
Password was copied to your clipboard.
```

FAQ
===

What is Password Hash?
----------------------

Password hash is a fingerprint of your master password.
Your master password is hidden in typing, so it is difficult to know if your password is correct, but the password hash should be a hint.

How Password is Generated?
--------------------------

The method to generate a password can be written in PHP like this:

```php
base64_encode(hex2bin(md5(password + "@" + domain)))
```
