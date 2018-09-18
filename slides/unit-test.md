### A simple unit test

```php
function formatCurrency($amount, $prefix = '$'): string
{
    return $prefix . number_format($amount/100, 2);
}
```

```
function testFormatCurrencyAppliesPrefix()
{
    $this->assertEquals(
        'USD $5.25',
        formatCurrency(525, 'USD $')
    );
}
```
<!-- .element: class="fragment" -->
