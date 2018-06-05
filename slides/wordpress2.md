### WordPress Core Test Suite

* <!-- .element: class="fragment" --> Test classes extend `WP_Core_TestCase`
* <!-- .element: class="fragment" --> Factories for posts, users, & more

```sh
$ wp scaffold plugin-tests
$ wp scaffold theme-tests
```
<!-- .element: class="fragment" -->

Note:

* Test classes will usually extend `WP_Core_TestCase`, which extends `PHPUnit\Framework\TestCase`
    - Handles setting up the WordPress environment
    - Includes handy generators for posts, taxonomy terms, users, and more
* For plugin and theme developers, WP-CLI can scaffold the necessary code
