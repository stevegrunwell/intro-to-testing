<pre><code class="hljs lang-php" style="max-height: none;">class MyTestCase extends PHPUnit\Framework\TestCase
{
    private $instance;

    public function setUp()
    {
        $this->instance = new MyApp(
            // Some complicated setup.
        );
    }

    public function testSomeMethodReturnsArray()
    {
        $this->assertInternalType(
            'array',
            $this->instance->someMethod()
        );
    }
}</code></pre>

Note:

In this example, maybe we have a MyApp class that needs some setup work; we can automatically instantiate it and save it to the private $instance property for each test.
