### Testing for errors

<pre class="fragment fragment-replacement" data-fragment-index="0"><code class="hljs lang-php fragment fade-out" data-fragment-index="1">public function testThrowsException()
{
    $this->expectException(DomainException::class);

    someFunction();
}</code><code class="hljs lang-php fragment fade-in" data-fragment-index="1">public function testThrowsException()
{
    try {
        someFunction();
    } catch (DomainException $e) {
        // Do other assertions, then return early.
        return;
    }

    $this->fail('Did not receive expected DomainException.');
}</code></pre>

Note:

* Sometimes, we also need to test that certain errors occur
    - Exceptions are thrown
    - PHP errors are triggered
* Second approach helps if you need to inspect the exception
