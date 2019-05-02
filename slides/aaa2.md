### Arrange - Act - Assert

```php
public function testHandlesDuplicateToppings()
{
    // Arrange.
    $pizza = new Pizza('large');
    $pizza->addTopping('pepperoni');
    $pizza->addTopping('pepperoni'); // Duplicate!
    $pizza->addTopping('sausage');

    // Act.
    $toppings = $pizza->getToppings();

    // Assert.
    $this->assertEquals(['pepperoni', 'sausage'], $toppings);
}
```

Note:

* Create a new, large pizza and add toppings
    - Maybe pepperoni was submitted twice by customers, and we want to make sure it only gets added once
* Next, call getToppings() for our Pizza object
    - We should only see two toppings: pepperoni (once) and sausage
