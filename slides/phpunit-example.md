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

* Unit test for the getCoffee() function
    - function returns Coffee object with given size + roast level
* Test within PHPUnit might look like this:
    - Call getCoffee() with 'large' size and 'light' roast
    - Assert we received an instance of Coffee, with a size of large and a light roast
