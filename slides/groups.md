### @group

Used to run tests of a similar nature, across suites & classes:

```php
/**
 * @group API
 * @group UserContent
 */
public function testIncludesPrivatePosts()
{
    // ...
}
```

```sh
$ phpunit --group=API
```
<!-- .element: class="fragment" -->

Note:

* The @group tag lets us group tests — no matter where they live — together
    - Really useful when different areas of the app need tested together
    - Completely user-defined, and test methods can belong to multiple groups
