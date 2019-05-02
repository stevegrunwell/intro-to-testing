## Stubbing APIs with Guzzle

```php
use GuzzleHttp\Client;
use GuzzleHttp\Handler\MockHandler;
use GuzzleHttp\HandlerStack;
use GuzzleHttp\Psr7\Response;

// Pre-determined HTTP responses
$mock = new MockHandler([
    new Response(200, [], json_encode(['title' => 'Some title'])),
]);

$client = new Client([
    'handler' => new HandlerStack::create($mock),
]);

// Inject $client wherever we need it!
```

Note:

If you're working with third-party APIs, you'll often want to stub the responses — remember, you're testing your app, not the API.

The Guzzle MockHandler lets us pre-determine the client responses, so we can verify that it's giving back known values.

Using dependency injection or a service resolver, we can inject this test-double for the Guzzle HTTP client wherever we need it!
