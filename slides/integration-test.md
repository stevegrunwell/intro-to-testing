### A simple integration test

```php
public function testFiltersPostsByAuthor()
{
    // Create two authors and generate posts for each.
    $authors = $this->generateAuthors(2);
    $postsA1 = $this->generatePostsForAuthor($author[0], 3);
    $postsA2 = $this->generatePostsForAuthor($author[1], 2);

    // Hit the "posts" API endpoint for posts from Author #1.
    $response = $this->get('/posts?author=' . $authors[0]);

    $this->assertCount(3, $response, 'Expected to see 3 posts.');
}
```

Note:

For this test, assume we have an API with a /posts endpoint, which can be filtered by author ID.

First, generate two authors, and assign some posts to each author.

If we hit the endpoint for author 1, we expect to see the three posts we assigned earlier.
