### Fixtures

<pre class="fragment-replacement"><code class="hljs lang-php fragment fade-out" data-fragment-index="0">public function setUp()
{
    // Set 'em up...
}

public function tearDown()
{
    // ...and knock 'em down.
}</code><code class="hljs lang-php fragment fade-in" data-fragment-index="0">public static function setUpBeforeClass()
{
    // Set 'em up (once)...
}

public static function tearDownAfterClass()
{
    // ...and knock 'em down (once).
}</code></pre>

Note:

* Enables common setup and tear-down actions to be run automatically before and after each test method
    - Really useful for integration tests
    - Can also use setUpBeforeClass() for things that only should be run once per test case
* Likewise, can be used for tearing things down
    - Also can use tearDownAfterClass()
* Can also use @before, @beforeClass, @after, and/or @afterClass
