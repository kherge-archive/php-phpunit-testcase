PHPUnit TestCase
================

[![Build Status](https://travis-ci.org/herrera-io/php-phpunit-testcase.png?branch=master)](https://travis-ci.org/herrera-io/php-phpunit-testcase)

A PHPUnit test case class and trait with additional functionality.

Summary
-------

The `TestCase` class and `Extras` trait provide additional methods for performing basic, repetitive tasks such as:

- creating and deleting temporary files and directories
- calling protected and private methods
- retrieving and setting protected and private properties

> **NOTE** Both `TestCase` and `Extras` are identical, except the former being a class and the latter being a trait.

Installation
------------

Add it to your list of Composer dependencies:

```sh
$ composer require herrera-io/phpunit-test-case=1.*
```

Usage
-----

### The `TestCase` class

```php
<?php

class MyTestCase extends Herrera\PHPUnit\TestCase
{
    // my tests
}
```

### The `Extras` trait

```php
<?php

class MyTestCase extends My\Own\Custom\TestCase
{
    use Herrera\PHPUnit\Extras;

    // my tests
}
```

> **NOTE** If your test class provides its own `tearDown()` method, make sure to call the class's or trait's `tearDown()` method as well. `TestCase` and `Extras` uses the tear down process to clean up temporary files and directories.