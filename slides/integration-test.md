### A simple integration test

```php
public function testFiltersPostsByAuthor()
{
    // Create two authors and generate posts for each.
    $bob   = $this->generateAuthors('Bob');
    $alice = $this->generateAuthor('Alice');

    $this->generatePostsForAuthor($bob, 2);
    $this->generatePostsForAuthor($alice, 3);

    // Hit the "posts" API endpoint for posts from Bob.
    $response = $this->get('/posts?author=' . $bob->id);

    $this->assertCount(2, $response, 'Expected to see 2 posts.');
}
```

Note:

For this test, assume we have an API with a /posts endpoint, which can be filtered by author ID.

First, generate two authors, and assign some posts to each author.

If we hit the endpoint for Bob, we expect to see the three posts we assigned earlier.
