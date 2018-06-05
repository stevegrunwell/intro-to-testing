### [Mockery](http://docs.mockery.io/)

Popular library for creating test doubles:

<pre class="fragment-replacement"><code class="hljs lang-php fragment fade-out" data-fragment-index="0">public function testHandlesEmptyOrderList()
{
    $api = Mockery::mock(Api::class)->makePartial();
    $api->shouldReceive('getOrders')
        ->once()
        ->andReturn([]);

    $this->assertEmpty($api->getRecentOrders());
}</code><code class="hljs lang-php fragment fade-in" data-fragment-index="0">public function testHandlesEmptyOrderList()
{
    $api = Mockery::spy(Api::class)->makePartial();

    $this->assertEmpty($api->getRecentOrders());

    $api->shouldHaveReceived()
        ->getOrders()
        ->once();
}</code></pre>

Note:

* While PHPUnit allows for some test doubles, Mockery is a popular alternative
    - Expressive interface for defining test doubles, their expectations, and responses
* API object should receive getOrders() exactly once and return an empty array
    - Will fail the test if getOrders() isn't called exactly once
* Spies let us adhere closer to Arrange - Act - Assert, but give us less control
