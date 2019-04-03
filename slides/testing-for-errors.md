### Testing for errors

<pre class="fragment fragment-replacement" data-fragment-index="0"><code class="hljs lang-php fragment fade-out" data-fragment-index="1">public function testThrowsException()
{
    try {
        someFunction();
    } catch (DomainException $e) {
        $this->assertSame(500, $e->getCode());
        $this->assertSame('Some error!', $e->getMessage());

        // Return early to avoid the $this->fail() call.
        return;
    }

    $this->fail('Did not receive expected DomainException.');
}</code><span class="fragment fade-out" data-fragment-index="2"><code class="hljs lang-php fragment fade-in" data-fragment-index="1">public function testThrowsException()
{
    $this->expectException(DomainException::class);
    $this->expectExceptionCode(500);
    $this->expectExceptionMessage('Some error!');

    someFunction();
}</code></span><code class="hljs lang-php fragment fade-in" data-fragment-index="2">/**
 * @expectedException        DomainException
 * @expectedExceptionCode    500
 * @expectedExceptionMessage Some error!
 */
public function testThrowsException()
{
    someFunction();
}</code></pre>

(Deprecated in PHPUnit 8.0)<!-- .element: class="fragment" data-fragment-index="2" -->

Note:

* Sometimes, we also need to test that certain errors occur
    - Exceptions are thrown
    - PHP errors are triggered
* Can manually set up a try/catch block, wherein we inspect the caught exception and fail the test if we don't catch it.
* The $this->expectException() methods let us set up these expectations
* Can also be written via DocBlock annotations
