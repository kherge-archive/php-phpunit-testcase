PHPUnit TestCase
================

[![Build Status](https://travis-ci.org/herrera-io/php-phpunit-testcase.png?branch=master)](https://travis-ci.org/herrera-io/php-phpunit-testcase)

A PHPUnit test case class with additional functionality.

Summary
-------

The `TestCase` class provides additional methods for performing basic, repetitive tasks such as:

- creating and deleting temporary files and directories
- calling protected and private methods
- retrieving and setting protected and private properties

Installation
------------

Add it to your list of Composer dependencies:

```sh
$ composer require herrera-io/phpunit-test-case=1.*
```

Usage
-----

To use `TestCase`, you extend it as you would an ordinary PHPUnit test case:

```php
<?php

class MyTestCase extends Herrera\PHPUnit\TestCase
{
    // my tests
}
```

If your test class provides its own `tearDown()` method, make sure to call the parent `tearDown()` method as well. `TestCase` uses the tear down process to clean up temporary files and directories.