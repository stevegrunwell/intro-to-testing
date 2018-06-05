### Bootstrapping

* <!-- .element: class="fragment" --> Loaded <u>before</u> the test suite
* <!-- .element: class="fragment" --> Great for loading dependencies

```php
// Load Composer dependencies.
require __DIR__ . '/../vendor/autoload.php';

// Do any other necessary setup work.
```
<!-- .element: class="fragment" -->

Note:

* In our phpunit.xml file, we specified a bootstrap file (tests/bootstrap.php), which will be loaded before our test suite
    - Great for installing dependencies or bootstrapping frameworks like WordPress
    - If you're strictly using autoloaders, use vendor/autoload.php as the bootstrap file
