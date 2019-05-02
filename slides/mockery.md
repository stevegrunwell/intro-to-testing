### [Mockery](http://docs.mockery.io/)

Popular library for creating test doubles:

```php
/**
 * @test
 */
public function no_orders_should_result_in_no_recent_orders()
{
    $api = Mockery::mock(Api::class)->makePartial();
    $api->shouldReceive('getOrders')
        ->once()
        ->andReturn([]);

    $this->assertEmpty($api->getRecentOrders());
}
```

Note:

* While PHPUnit allows for some test doubles, Mockery is a popular alternative
    - Expressive interface for defining test doubles, their expectations, and responses
* API object should receive getOrders() exactly once and return an empty array
    - Will fail the test if getOrders() isn't called exactly once
