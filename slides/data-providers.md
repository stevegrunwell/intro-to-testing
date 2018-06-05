### Data providers

<pre class="fragment fragment-replacement" data-fragment-index="0"><code class="hljs lang-php fragment fade-out" data-fragment-index="1">/**
 * @dataProvider myDataProvider()
 */
public function testMyFunction($expected, $actual)
{
    $this->assertEquals($expected, myFunction($actual));
}

public function myDataProvider()
{
    return [
        'Description of case 1' => ['foo', 'bar'],
        'Description of case 2' => ['bar', 'baz'],
    ];
}</code><code class="hljs lang-php fragment fade-in" data-fragment-index="1">/**
 * @testWith ["foo", "bar"]
 *           ["bar", "baz"]
 */
public function testMyFunction($expected, $actual)
{
    $this->assertEquals($expected, myFunction($actual));
}</code></pre>

Note:

* Lets you pass multiple variants to the same test method
* @dataProvider tag lets you reference another method, which should return an array of scenarios
* Can also use @testWith and pass them directly in the DocBlock
    - Cannot call functions or use constants
