```php
function getCoffee(string $size, string $roast = 'medium'): Coffee
{
    $coffee = new Coffee;
    $coffee->setSize($size);
    $coffee->setRoast($roast);

    return $coffee;
}
```

```php
public function testGetCoffee()
{
    $coffee = getCoffee('large', 'light');

    $this->assertInstanceOf(Coffee::class, $coffee);
    $this->assertSame('large', $coffee->getSize());
    $this->assertSame('light', $coffee->getRoast());
}
```
<!-- .element: class="fragment" -->

Note:

Imagine we have a getCoffee() function, which gives us a Coffee object with a given size and roast level.

In our test method, we might test that the function returns the Coffee object we described — large and with a light roast.
