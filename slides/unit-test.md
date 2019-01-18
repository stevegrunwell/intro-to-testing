### A simple unit test

```php
function formatCurrency(int $cents, string $prefix = '$'): string
{
    return $prefix . number_format($cents/100, 2);
}
```

```php
function testFormatCurrencyAppliesPrefix()
{
    $this->assertEquals(
        'USD $5.25',
        formatCurrency(525, 'USD $')
    );
}
```
<!-- .element: class="fragment" -->
