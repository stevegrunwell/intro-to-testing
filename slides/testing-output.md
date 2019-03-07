### Testing output

```php
public function greet()
{
    printf('Hello, %s!', $this->first_name);
}
```
<!-- .element: class="fragment" data-fragment-index="0" -->

<div class="fragment-replacement">
    <pre class="fragment" data-fragment-index="1"><code class="hljs lang-php fragment fade-out" data-fragment-index="2">public function testRendersHelloWorld()
{
    $user = new User([
        'first_name' => 'Tony',
        'last_name'  => 'Stark',
    ]);

    ob_start();
    $user->greet();
    $output = ob_get_clean();

    $this->assertSame('Hello, Tony!', $output);
}</code><code class="hljs lang-php fragment fade-in" data-fragment-index="2">public function testRendersHelloWorld()
{
    $user = new User([
        'first_name' => 'Tony',
        'last_name'  => 'Stark',
    ]);

    $this->setExpectedOutput('Hello, Tony!');

    $user->greet();
}</code></pre></div>
</div>

Note:

* Imagine a simple greet() method on a User object
    - Doesn't return anything, just prints the output
* Could capture the output buffer to make assertions, OR
* We can use setExpectedOutput() to set the expectation
