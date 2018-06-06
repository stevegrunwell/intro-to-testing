### phpunit.xml

```xml
<?xml version="1.0" encoding="UTF-8"?>
<phpunit bootstrap="tests/bootstrap.php">
    <testsuites>
        <testsuite name="Unit">
            <directory suffix="Test.php">./tests/Unit</directory>
            <exclude>./tests/Unit/SampleTest.php</exclude>
        </testsuite>
    </testsuites>
    <php>
        <!-- Set constants, environment variables, etc. -->
    </php>
</phpunit>
```

Note:

* The phpunit.xml file contains the configuration for PHPUnit
    - Bootstrap file (more in a second)
    - Define test suites
    - Exclusions
    - PHP configuration
