### Fixtures

```php
public function setUp()
{
    // Set 'em up...
}
```
<!-- .element: class="fragment" -->

```php
public function tearDown()
{
    // ...and knock 'em down.
}
```
<!-- .element: class="fragment" -->

Note:

* Enables common setup actions to be run automatically before each test method
    - Really useful for integration tests
    - Can also use setUpBeforeClass() for things that only should be run once per test case
* Likewise, can be used for tearing things down
    - Also can use tearDownAfterClass()
* Can also use @before, @beforeClass, @after, and/or @afterClass
