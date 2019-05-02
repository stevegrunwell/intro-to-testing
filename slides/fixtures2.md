<pre><code class="hljs lang-php" style="max-height: none;">class MyTestCase extends PHPUnit\Framework\TestCase
{
    protected $instance;

    public function setUp(): void
    {
        $this->instance = new MyApp(
            // Some complicated setup.
        );
    }

    public function testSomeMethodReturnsArray()
    {
        $this->assertIsArray($this->instance->someMethod());
    }
}</code></pre>

Note:

In this example, maybe we have a MyApp class that needs some setup work; we can automatically instantiate it and save it to the protected $instance property for each test.
