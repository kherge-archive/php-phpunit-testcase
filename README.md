PHPUnit TestCase
================

[![Build Status](https://travis-ci.org/herrera-io/php-phpunit-testcase.png?branch=master)](https://travis-ci.org/herrera-io/php-phpunit-testcase)

A PHPUnit test case class with additional functionality.

Usage
-----

```php
use Herrera\PHPUnit\TestCase;

class MyTest extends TestCase
{
    public function testCallProtected()
    {
        $object = new MyClass();

        $this->callMethod($object, 'protectedMethod', array('args'));
    }
}
```