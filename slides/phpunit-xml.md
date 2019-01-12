### phpunit.xml

```xml
<?xml version="1.0" encoding="UTF-8"?>
<phpunit bootstrap="vendor/autoload.php">
    <testsuites>
        <testsuite name="Unit">
            <directory suffix="Test.php">./tests/Unit</directory>
        </testsuite>
    </testsuites>
    <php>
        <!-- Set constants, environment variables, etc. -->
    </php>
</phpunit>
```

Note:

* The phpunit.xml file contains the configuration for PHPUnit
    - Bootstrap file (typically vendor/autoload to ensure dependencies can be autoloaded)
    - Define test suites
    - PHP configuration
